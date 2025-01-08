# Networking Concepts Quiz

## IP Subnetting

1. Given a network 203.0.113.0/24, calculate:
   - The number of usable host addresses
   - The broadcast address
   - The first and last usable host addresses

2. You need to create 6 subnets from 198.51.100.0/16. What prefix length should you use to ensure each subnet has at least 1000 usable addresses?

3. In a network 45.67.0.0/22:
   - What is the subnet mask in decimal notation?
   - How many /24 networks can you create from this network?

4. A host has IP 194.12.5.130/27. What is its network address?

## NAT and Network Design

5. Given this network diagram:
```
Internet --- [Router with NAT] --- [Switch] --- Server (203.0.113.100)
```
Explain why an external client cannot directly initiate a connection to the server.

6. In a network using NAT:
   - Server: 198.51.100.10
   - Router internal: 198.51.100.1
   - Router external: 203.0.113.5
Design the necessary NAT configuration to make the server's HTTP service (port 80) accessible from the internet.

7. Why does FTP in passive mode require special NAT handling? Explain the challenges with dynamic port allocation.

8. Your company has two offices connected via site-to-site VPN, both using 192.168.1.0/24 internally. What problems might arise? Propose a solution.

## ARP

9. A host sends an ARP request for IP 192.168.1.100. What is:
   - The destination MAC address
   - The source MAC address
   - The packet's Layer 2 broadcast domain scope

10. Explain the security implications of ARP spoofing in a switched network. How can it be prevented?

11. When does a host update its ARP cache? List three specific scenarios.

12. What problems can arise from having too many hosts in a single ARP broadcast domain?

## DHCP

13. A client boots up and has no IP address. List all DHCP messages exchanged in sequence, including:
    - Message types
    - Source and destination IP/MAC addresses
    - Key information in each message

14. Design a DHCP configuration for:
    - Network: 203.0.114.0/24
    - Reserved first 20 addresses for servers
    - Lease time: 8 hours
    - DNS servers: 8.8.8.8, 8.8.4.4

15. Why might a DHCP server send NAK to a client? Give two specific scenarios.

16. In a network with multiple VLANs, how does DHCP relay work? Explain the packet flow.

## MAC Address Learning

17. A bridge has just booted up. Describe step-by-step how its MAC address table gets populated when:
    - Host A (00:11:22:33:44:55) sends to Host B (66:77:88:99:AA:BB)
    - Host B replies to Host A

18. What happens when:
    - A bridge receives a frame with an unknown destination MAC?
    - The MAC address table is full?
    - A MAC address hasn't been used for 5 minutes?

19. In a network with redundant bridges, why is MAC address learning problematic? How does STP help?

20. A host moves from one switch port to another. Describe:
    - How the switch detects this
    - What updates occur in the MAC address table
    - Potential issues if this happens frequently