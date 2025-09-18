
 Protocol (STP), and BPDU Guard using Cisco Packet Tracer. The lab shows how to segment traffic
 with VLANs, enable router-on-a-stick for routing, prevent loops with STP, and secure access ports
 using BPDU Guard.
 Lab Topology:- 
 Router0 (2911)
 Switch0 (2960
 Switch1 (2960)
 PCs: PC0 (VLAN 10), PC1 (VLAN 20), PC2 (VLAN 20)
 VLAN & IP Plan:
 VLAN 10: 192.168.10.0/24 → Gateway 192.168.10.1
 VLAN 20: 192.168.20.0/24 → Gateway 192.168.20.1
 Configuration Steps
 1. On Switch0 (main switch):- Create VLANs 10 & 20 and assign ports.- Configure trunk to Router0 (Gig0/0) and Switch1.- Enable PortFast and BPDU Guard on access ports.
 2. On Switch1 (secondary switch):- Create VLANs 10 & 20.- Assign access port for PC2.- Configure trunk links back to Switch0.
 3. On Router0 (Router-on-a-Stick):- Configure Gig0/0.10 with encapsulation dot1Q 10, IP 192.168.10.1/24.- Configure Gig0/0.20 with encapsulation dot1Q 20, IP 192.168.20.1/24.
 Verification
 • Check Router sub-interfaces with show ip interface brief.
 • Verify trunk links with show interfaces trunk on switches.
 • Assign IP addresses to PCs and test ping between VLANs.
 • Verify STP operation with show spanning-tree. One link should be blocked.
 • Test BPDU Guard by connecting a switch to an access port. It should go err-disabled.
 Conclusion:
 This lab successfully demonstrates Inter-VLAN routing via Router-on-a-Stick, loop prevention with
 Spanning Tree Protocol, and port security with BPDU Guard.

