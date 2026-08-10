# Lab 4 — Site-to-Site VPN (IPSec) Basics

Goal: Establish a simple IPsec site-to-site VPN between two virtual routers.

Topology: Router A (Site A) <--- Internet --- Router B (Site B)

Steps:
1. Configure public IPs (or use NAT with port forwarding in labs).
2. On both routers, create IKE policy (pre-shared key) and IPsec transform set.
3. Define crypto map and apply to the WAN interface.
4. Create interesting traffic ACLs and route traffic through the tunnel.

Verification:
- Use `show crypto isakmp sa` and `show crypto ipsec sa` to confirm tunnel state.
- Ping private hosts across the VPN.
