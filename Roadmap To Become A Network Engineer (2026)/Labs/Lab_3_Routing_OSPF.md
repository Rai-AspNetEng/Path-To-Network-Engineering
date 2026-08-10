# Lab 3 — OSPF Routing Lab

Goal: Configure OSPF in a multi-area/single-area topology and verify route propagation.

Topology: 3 routers connected in a triangle; each router has a LAN

Steps:
1. Assign IPs to router interfaces.
2. Enable OSPF (process 1) and advertise connected networks.
3. Verify OSPF neighbors and routing table (`show ip ospf neighbor`, `show ip route ospf`).
4. Test failover by shutting an interface and observing reroute.

Verification:
- Ping across LANs through OSPF paths.
- Confirm LSDB (`show ip ospf database`).
