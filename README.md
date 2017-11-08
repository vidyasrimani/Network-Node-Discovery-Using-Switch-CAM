
Network connectivity discovery is an extensively studied area, and there are many interesting mechanisms such as ping, traceroute, DNS, address resolution protocol (ARP), and SNMP available to discover network elements and the connectivity among them. 
Traceroute is a computer network diagnostic tool for displaying the route (path) and measuring transit delays of packets across an Internet Protocol (IP) network. The history of the route is recorded as the round-trip times of the packets received from each successive host (remote node) in the route (path); the sum of the mean times in each hop indicates the total time spent to establish the connection. Traceroute proceeds unless all sent packets are lost more than twice, then the connection is lost and the route cannot be evaluated. Ping, on the other hand, only computes the final round-trip times from the destination point.
Ping or Packet Internet Gopher is a computer network administration software utility used to test the reachability of a host on an Internet Protocol (IP) network and to measure the round-trip time for messages sent from the originating host to a destination computer. The name comes from active sonar terminology which sends a pulse of sound and listens for the echo to detect objects underwater. Ping operates by sending Internet Control Message Protocol (ICMP) echo request packets to the target host and waiting for an ICMP response. In the process it measures the time from transmission to reception (round-trip time) and records any packet loss. The results of the test are printed in the form of a statistical summary of the response packets received, including the minimum, maximum, and the mean round-trip times, and sometimes the standard deviation of the mean.
The Address Resolution Protocol (ARP) is a telecommunication protocol used for resolution of network layer addresses into link layer addresses, a critical function in multiple-access networks. ARP was defined by RFC 826 in 1982. It is Internet Standard STD 37. It is also the name of the program for manipulating these addresses in most operating systems. ARP is used to convert a network address (e.g. an IPv4 address) to a physical address such as an Ethernet address (also known as a MAC address).
There have been some efforts made by Cisco to standardize the Physical Network Topology Identification and Discovery (PTOPO-MIB) in RFC 2922, however Cisco is the only vendor supporting this. There are various commercial tools such as HP OpenView, IBM’s Tivoli, and AdventNet OpManager but these show only L3 Level switches. Apart from these commercial ventures, there has been much effort made by the research community in this direction. 
A good survey and mechanism was proposed to discover network nodes by combining ping, traceroute, SNMP, DNS, and ARP. However, these methods could discover only L3 level switches, though it was proved that SNMP performs better than all other mechanisms. Another mechanism is proposed that is heterogeneous, irrespective of any kind of network, but this mechanism requires ICMP spoofing in order to get complete forwarding table, which is not allowed in most of today’s networks.

# Disadvantages of Existing Systems
•	It is unable to discover a variety of devices simultaneously. These include L2 and L3 switches.
•	It fails to provide details of SNMP MIBs required for gathering information.
•	The current algorithms such as Ping, Traceroute, DNS, and ASP are time consuming and resource intensive.
•	The state of network nodes may change during the discovery process and faulty information may be displayed.
•	Current systems do not account for the presence of VLANs in a network. This usually leads to networks with cycles that may interfere with the existing discovery process.
•	Existing algorithms are also extensive and complex. 

# PROBLEM STATEMENT
A wired Local Area Network (LAN) may spread across various buildings and floors for connecting computers and servers. The LAN would normally consist of network switches which are remotely manageable. These networks also exist with different topologies. As the number of network nodes increases, the complexity of monitoring, maintaining and troubleshooting also increases.
With access to information of nodes in a network, network managers are better able to react to and prevent problems. Hence, complete information about the network devices and links is to be maintained for efficient network management. 
A comprehensive overview of the network and the nodes attached to it is essential to maintain the network. The knowledge of these nodes allows administrators to anticipate problems and plan for them before services are impacted. To ensure security, isolating the nodes is essential to exactly locate the switch port to which a node is connected. 

# PROPOSED SYSTEM 
#Scope of the System
The proposed system maps the switch port of the all the nodes and finds information related to the node. It also helps network engineers identify the switch port to which a device is connected and thus eliminates the need of manually tracing the network cables. As the approach of the system is mainly based on Simple Network Management Protocol (SNMP), the Management Information Base (MIB) is analysed and used extensively.
It discovers the devices plugged into each port of a specified switch using Content Addressable Memory (CAM) entries of switches. This is useful for system and network engineers to gain visibility into the IP, MAC, VLAN, status and availability of ports. Since this is a real time discovery and not vendor specific, the administrators can also view the operational status and speed of each port.
# Objective of the System
•	Used to identify the Switch Port to which the node is connected
•	Provides an easy and fast mechanism to retrieve information corresponding to the specific node in the network
•	To facilitate ease of usage for network administrators to monitor the nodes of a large wired network
•	Gives status of the ports, VLANs, switches and nodes within a network
•	Contains a comprehensive list of all the nodes that are currently active and inactive
•	Provides access only to network administrators

# Features of the Proposed Solution	
•	The proposed system is specific to Indian Space Research Organisation’s (ISRO) network
•	If the host IP address and the specific MIB required for Community String Indexing are provided for a network, then this solution would be able to retrieve the node status of its network
•	The solution is able to obtain information from L2 Switches, L3 Switches and D Link Switches that make up the network as a whole

# Limitations of the Proposed System
•	Is unable to provide the end to end path of a specific connection
•	Cannot be implemented on a network that does not completely conform to SNMP standards
•	Cannot discern wireless nodes attached to the network
•	Does not show the topology of the network


