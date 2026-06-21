# Enterprise Network Isolation & Firewall Hardening Lab

A hands-on engineering lab focused on building an isolated enterprise network topology, deploying a secure Linux workstation client, and enforcing stateful traffic-filtering policies at the gateway boundary.

## 🛠️ Infrastructure & Tools
* **Hypervisor:** Oracle VirtualBox
* **Boundary Firewall:** Netgate pfSense (FreeBSD)
* **Secure Client:** Ubuntu Desktop 24.04 LTS
* **Internal Network Switch:** Isolated Virtual Bus (`Internal-Secure-Bus`)

---

## 🗺️ Network Topology
The environment is engineered to enforce strict network segmentation. The secure client workspace has zero direct connection to the public internet WAN and relies entirely on the firewall gateway for routing and policy enforcement.

```text
       [ External WAN / Internet ]
                   │
        [ pfSense Boundary Firewall ]
                   │
         [ Internal-Secure-Bus ]
                   │
         [ Ubuntu Workstation ]
             (192.168.1.101)
