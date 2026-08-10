# Lab 5 — Network Automation: Ansible Playbook

Goal: Use Ansible to collect device facts and back up device configs.

Prerequisites: controller machine with Ansible and network access to lab routers/switches.

Steps:
1. Install required collections: `ansible-galaxy collection install cisco.ios` (or vendor-specific)
2. Create `inventory.yml` with device hosts and connection variables.
3. Write a playbook `backup-config.yml` that connects via `network_cli` and uses `ios_command`/`ios_config` modules to fetch `show run` and save to files.
4. Run the playbook and verify backup files are created.

Example snippets:
```yaml
- hosts: routers
  gather_facts: no
  connection: network_cli
  tasks:
    - name: show running-config
      ios_command:
        commands: show running-config
      register: running

    - name: save config to file
      copy:
        content: "{{ running.stdout[0] }}"
        dest: "./backups/{{ inventory_hostname }}.cfg"
```

Verification:
- Confirm `backups/` contains device config files.
