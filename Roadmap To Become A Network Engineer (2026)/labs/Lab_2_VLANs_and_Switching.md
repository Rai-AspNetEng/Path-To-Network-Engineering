# Lab 2 — VLANs & Basic Switching

Goal: Build VLANs, configure trunking, and verify inter-VLAN routing.

Topology: 2 switches, 1 router (or L3 switch), 4 hosts

Steps:
1. Create VLANs: 10 (Sales), 20 (Engineering), 30 (Guest)
2. Assign access ports to VLANs on switches.
3. Configure trunk (802.1Q) between switches and to the router.
4. On the router, configure sub-interfaces for each VLAN with IP addresses.
5. Verify MAC address tables and VLAN membership (`show mac address-table`, `show vlan brief`).

Verification:
- From hosts on different VLANs, test connectivity to their gateway and to other VLANs (if routing is enabled).
- Use `show interfaces trunk` to confirm trunking.
