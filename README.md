# Understanding-the-Importance-of-Routers-in-Networking
Overview:

In this experiment, I expanded on my previous exploration of switches and learned why routers are essential for communication between different networks. Using Cisco Packet Tracer, I tested scenarios where I attempted to connect devices across networks with and without a router, and observed how routers facilitate communication. I also explored the role of a DNS server in resolving domain names and how ARP messages play a key role in communication.

Key Insights

	1.	Why We Need Routers (Switch vs. Router):
 
	•	Switch-to-Switch Connection Attempt:
	•	I connected two switches from different networks in Cisco Packet Tracer without a router.
	•	When I tried to send a message from one device (Johnny) on one switch to a device (Larry) on another, the message failed repeatedly.
	•	This happened because:
	•	Devices on separate networks have different IP address groups.
	•	The switch sent an ARP (Address Resolution Protocol) message to locate the destination device’s MAC address.
	•	The only response it received was from the gateway of the network, and the communication could not proceed.
	•	Conclusion: A router is necessary to connect different networks and facilitate communication.
	
 2.	How Routers Work:
 
	•	After adding a router to the setup:
	•	When Johnny tried to ping networklarry.com on the other network, an ARP request was sent to the router.
	•	The router responded with information about the destination IP address and communicated with the other network to locate the device (Larry).
	•	The message was successfully delivered, proving that a router acts as a bridge between different networks.
	
 3.	Adding a DNS Server:
 	
	•	I added a DNS server to Johnny’s network to test domain name resolution.
	•	When Johnny searched for networklarry.com:
	•	An ARP message was broadcast to all devices on the network.
	•	The DNS server received the request, resolved the domain name to its corresponding IP address, and sent the response back to Johnny through the switch.
	•	Note: I had to manually configure the DNS server by assigning it an IP address for it to function correctly.
	
 4.	Exploring Router CLI Commands:
    
	•	I used the CLI (Command-Line Interface) on the router to view the routing table with the command:

show ip route

This command displayed a comprehensive list of IP addresses and routing paths, illustrating how the router keeps track of all reachable networks.

Practical Commands Used: 

1. Ping Command
   
- To test connectivity:
  ping <destination IP or domain>

2. Router Routing Table

- To view the IP address mappings and routing information :
  show ip route

Lessons Learned

	•	Routers vs. Switches: Switches handle communication within the same network using MAC addresses, while routers are essential for communication between different networks by managing IP addresses.
	•	ARP and DNS: ARP resolves IP addresses to MAC addresses, and DNS resolves domain names to IP addresses. Both work together to enable smooth communication.
	•	Practical Router Usage: Configuring routers and DNS servers is key to ensuring proper network communication and domain resolution.

  

