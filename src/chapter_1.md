# Introduction and Basic Terminology

It's essential to understand the "Open Systems Interconnection" (OSI) model:

<div style="text-align: center;">

  ![OSI Diagram](https://upload.wikimedia.org/wikipedia/commons/0/0e/Layers_of_OSI_modles.png)

</div>

The OSI model provides a standardized approach for organizing the functions of a communication system into layers, making it easier to understand and manage complex networking systems.

> The IP address works at layer 3
>
> The MAC address works at layer 2 (unique id key set in every device that connects to some network by the manufacturer)

# Physical/Layer 1 Devices

- MODEM 🠲 A modem (modulator-demodulator) is a device that converts digital signals from a computer into analog signals for transmission over a telephone line, and vice versa, to allow for communication with other computers.

- HUB 🠲 Connects multiple network devices together and allows them to share a common network connection. Data sent to a hub is transmitted to all connected devices, regardless of the intended recipient. (Not used nowadays)

# Datalink/Layer 2 Devices

- Switch 🠲 Connects multiple devices together on a computer network. Unlike a hub, a switch selectively directs data to only the intended recipient, rather than broadcasting data to all connected devices. This makes switches more efficient than hubs and enables them to support higher network speeds.

- WAP (Wireless Access Point) 🠲 Allows Wi-Fi enabled devices to connect to a wired network. It acts as a bridge between a Wi-Fi network and a wired Ethernet network, providing wireless access to the Internet and other network resources. WAPs typically include a radio transceiver, an antenna, and a network interface (such as Ethernet) to connect to a wired network.

# Network/Layer 3 Devices

- Multilayer Switch 🠲 Provides the functionality of both a switch and a router. It operates at multiple layers of the OSI model, typically including layers 2, 3, and 4, to provide advanced switching and routing capabilities. Multilayer switches are often used in enterprise networks to provide a high level of network security, segmentation, and performance. They can also be used for network virtualization and for implementing various network protocols and services, such as Quality of Service (QoS) and access control.

- Router 🠲 Forwards data packets between computer networks. Uses routing tables and protocols to determine the best path for data to travel from its source to its destination. Routers are commonly used in home and business networks to connect devices to the Internet and to provide network segmentation and security. They can also be used to connect multiple networks together to form larger, more complex networks.

# Security Techniques 

## Firewall 

A firewall controls incoming and outgoing network traffic based on predetermined security rules. It operates at the network layer (layer 3) or application layer (layer 7) of the OSI model, and its main function is to prevent unauthorized access to a network while allowing authorized communication. Firewalls can be hardware-based, software-based, or a combination of both, and are commonly used to protect computer networks, servers, and other sensitive resources from malicious attacks and unauthorized access.

Stateless and stateful inspection are two methods used by firewalls to inspect network traffic and enforce security policies.

Stateless inspection, also known as packet filtering, is a basic firewall technique that examines individual network packets and makes a decision based on their source and destination addresses, ports, and protocols. This type of inspection does not keep track of the connection state between packets and does not provide information about the flow of data between the source and destination.

Stateful inspection, also known as dynamic packet filtering, is a more advanced firewall technique that not only inspects individual packets, but also keeps track of the connection state between packets. This allows the firewall to make decisions based on the context of the connection, such as the sequence and acknowledgment numbers of packets, and to determine if a packet is part of an established connection or if it is a new, potentially malicious connection.

Stateful inspection provides a higher level of security and is often used in enterprise networks to provide deep packet inspection and advanced security features, such as application-level filtering and intrusion detection.

## (IDS) Intrusion Detection System

An IDS monitors a computer network or system for malicious activity or policy violations. It operates by analyzing network traffic, system logs, and other data sources to detect and alert administrators to potential security threats. IDSs can be either host-based, meaning they are installed on individual network devices, or network-based, meaning they monitor network traffic at various points in the network.

There are two main types of IDS: signature-based and anomaly-based. Signature-based IDSs use a database of known attack patterns or signatures to identify potential security threats. Anomaly-based IDSs, on the other hand, use statistical and behavioral analysis to identify unusual or suspicious activity on the network.

IDSs play an important role in network security by providing real-time visibility into network activity and by detecting potential security threats before they can cause significant damage. They can also provide valuable information for incident response and forensic analysis.

## (IPS) Intrusion Prevention System

An IPS monitors a computer network or system for malicious activity or policy violations, and takes action to prevent or block the activity. IPSs operate similarly to IDSs, but with the addition of the ability to actively prevent and block malicious activity.

An IPS operates by analyzing network traffic, system logs, and other data sources to identify potential security threats, and then takes action to stop the attack, such as blocking the malicious traffic or quarantining the affected device. IPSs can be either host-based, meaning they are installed on individual network devices, or network-based, meaning they monitor network traffic at various points in the network.

IPSs play an important role in network security by providing real-time protection against a wide range of security threats, including malware, exploits, and unauthorized access. They can also provide valuable information for incident response and forensic analysis.

## (VPN) Virtual Private Network

Creates a secure and encrypted connection over a public or untrusted network, such as the Internet. VPNs are commonly used to provide remote employees, business partners, and other users with secure access to a company's network and resources, or to allow users to access restricted content or services from anywhere in the world.

A VPN works by creating a virtual tunnel between a VPN client, such as a laptop or mobile device, and a VPN server. All data transmitted through this tunnel is encrypted and secure, even when the client and server are located in different parts of the world. This makes it possible for users to securely access sensitive information and resources, even when they are not connected to the company's network.

VPNs can be implemented using various technologies and protocols, including Internet Protocol Security (IPSec), Point-to-Point Tunneling Protocol (PPTP), and Layer 2 Tunneling Protocol (L2TP). They can also be integrated with other security technologies, such as firewalls and intrusion prevention systems, to provide a comprehensive security solution.

# Optimization Techniques 

## Load Balancer

A load balancer is a network device that distributes incoming network traffic across multiple servers or resources to optimize resource utilization, minimize response time, and increase overall system reliability. Load balancers operate at the network layer (layer 4) of the Open Systems Interconnection (OSI) model and use various algorithms, such as round-robin, least connections, and IP hash, to distribute incoming traffic across available resources.

They play a critical role in modern networks and cloud computing environments by allowing organizations to scale their applications and services to meet increasing demands. By distributing incoming traffic across multiple resources, load balancers help to ensure that no single resource becomes overwhelmed, improving overall system performance and reliability.

Load balancers can also provide additional benefits, such as SSL offloading, health monitoring, and traffic management, that make it easier to manage and scale complex network environments. They are commonly used in enterprise networks, web-based applications, and cloud computing environments to ensure high availability and performance of critical applications and services.

## Proxy Server

A proxy server is a server that acts as an intermediary between a client and another server, typically to provide security, anonymity, and access control. A proxy server receives requests from clients and makes requests to servers on behalf of clients. The results are then returned to clients.

They can be used for several purposes, including:

> Security: By routing client requests through a proxy server, the server's IP address is hidden from the servers being requested, providing a layer of anonymity and security.
> 
> Access control: Proxy servers can be used to restrict access to specific resources based on client IP addresses or other criteria.
> 
> Caching: A proxy server can cache frequently requested resources, reducing the need to request the same resource multiple times, improving response times and reducing network traffic.
> 
> Bypassing restrictions: A proxy server can be used to bypass firewalls, filters, and content restrictions, allowing clients to access restricted resources.

Proxy servers can be either transparent, meaning they do not alter the client's request, or anonymous, meaning they modify the client's request to provide a layer of anonymity. They can be deployed on the network perimeter or on individual hosts and can be used by individual users or organizations.

When a client device connects to the internet through a proxy server, all its requests and data are sent to the proxy server first. The proxy server then makes the requests on behalf of the client device and returns the response back to the client device. This way, the proxy server acts as an intermediary between the client device and the internet, and the client device's IP address and other identifying information is hidden from the internet.

There are several types of proxy servers, including:

> HTTP proxy: used to cache web content and filter incoming requests based on URL, IP address, and other criteria.
> 
> SOCKS proxy: used to provide anonymous access to the internet and bypass access restrictions.
> 
> Reverse proxy: used to provide load balancing, encryption, and security for web-based applications and services.
> 
> Transparent proxy: used to monitor and filter incoming network traffic, and can be used for content filtering and security.

# Network Devices and Authentication

## (NIC) Network Interface Card

Is a hardware component that connects a computer to a network. It provides a physical interface between the computer and the network cable, allowing the computer to send and receive data over the network.

NICs play a critical role in networking by providing the physical and logical connection between computers and the network. They are responsible for transmitting and receiving data, as well as converting the data into a format that can be transmitted over the network. NICs can also be configured with various settings, such as IP addresses, subnet masks, and gateway addresses, to control how the computer interacts with the network. It works at layer 1 and 2.


## (RADIUS) Remote Authentication Dial-In User Service

RADIUS works by receiving authentication and authorization requests from network access servers (NASs), such as routers or switches, and forwarding these requests to a central RADIUS server. The RADIUS server then authenticates the user and authorizes or denies the request based on the user's credentials and the organization's security policies.

## (TACACS+) Terminal Access Controller Access Control System Plus

Is a protocol used for remote authentication and authorization of network devices. TACACS+ provides centralized authentication, authorization, and accounting (AAA) services for network devices, such as routers, switches, and firewalls.

## (RAS) Remote Access Service

Provides a secure and reliable connection for remote access to network resources, such as file servers, printers, and applications.

## Web Services and Unified Voice Services(VoIP)