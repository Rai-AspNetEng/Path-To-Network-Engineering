# Lab 1 — Subnetting & IP Planning

Goal: Design subnets for a small office and verify addressing.

Topology: single router, three LANs (Sales, Engineering, Guest)

Requirements:
- Sales: 50 hosts
- Engineering: 120 hosts
- Guest: 30 hosts

Steps:
1. Choose an appropriate private network block (e.g., 192.168.0.0/22)
2. Use VLSM to allocate subnets:
   - Engineering: /25 (126 hosts)
   - Sales: /26 (62 hosts)
   - Guest: /27 (30 hosts)
3. Configure addresses on router sub-interfaces or separate interfaces.
4. Configure DHCP pools for each subnet (optional).

Verification:
- From hosts, ping gateway and other VLANs (if routed).
- Use `ip route` (or `show ip route`) to verify routing entries.

Hints: practice manual calculations, then validate with an online CIDR tool or `ipcalc`.
