# DHCP

DHCP (Dynamic Host Configuration Protocol) is a network protocol used to dynamically assign IP addresses to devices on a network. DHCP eliminates the need for manual configuration of IP addresses and other network settings on individual devices, by automatically providing these settings to devices as they connect to the network.

When a device connects to a network, it sends a broadcast message requesting an IP address. The DHCP server, typically located on a network router or dedicated server, receives the request and assigns an IP address to the device, along with the subnet mask, default gateway, and DNS server information.

DHCP provides several benefits over manual IP address assignment:

> Scalability: DHCP makes it easy to manage and scale large networks by automatically assigning IP addresses to new devices as they join the network.
>
> Reduced errors: DHCP eliminates the risk of manual configuration errors and ensures that all devices on the network have valid IP addresses and other network settings.
>
> Centralized management: DHCP provides a centralized location for managing network settings, making it easier to enforce consistent policies across the network.

## Process 

1.  Device request: When a device connects to a network, it sends a broadcast message requesting an IP address.

2.  DHCP server discovery: The DHCP server listens for broadcast requests and responds to the device, indicating that it is available to provide an IP address.

3.  Request for IP address: The device sends a request to the DHCP server for an IP address and other network configuration information.

4.  Offer from DHCP server: The DHCP server sends an offer to the device, including an available IP address, subnet mask, default gateway, and DNS server information.

5.  Request and acknowledgement: The device accepts the offer and sends a request to the DHCP server to confirm the assigned IP address. The DHCP server sends an acknowledgement, confirming the assignment.

6.  IP address assignment: The device is now assigned the IP address, subnet mask, default gateway, and DNS server information provided by the DHCP server.

7.  Renewal: The device will periodically request to renew the IP address assignment from the DHCP server. If the DHCP server is available and the IP address is still available, the renewal is granted and the IP address assignment remains unchanged. If the DHCP server is not available or the IP address has been assigned to another device, the device must request a new IP address.

## The Subnet Mask

The subnet mask is an important part of the network configuration information that is assigned by the DHCP server. The subnet mask is a binary mask that defines the boundary between the network portion and the host portion of an IP address. The subnet mask is used to determine which portion of the IP address represents the network and which portion represents the host.

For example, in a network with IP addresses in the range of 192.168.1.0 to 192.168.1.255, the subnet mask might be 255.255.255.0. This subnet mask defines that the first three octets of the IP address (192.168.1) represent the network portion and the last octet (0-255) represents the host portion. This allows devices on the network to route data to other devices on the same network and to devices on other networks.

## Static vs Dynamic

Static IP and dynamic IP are two methods of assigning IP addresses to devices on a network.

Static IP: A static IP address is a fixed, unchanging IP address assigned manually to a device. This means that every time the device connects to the network, it will be assigned the same IP address. Static IP addresses are useful for devices that need to be accessible from the Internet, such as web servers, email servers, and file servers, as they provide a permanent and easily accessible address for these devices.

Dynamic IP: A dynamic IP address is an IP address that is assigned to a device dynamically, typically by a DHCP (Dynamic Host Configuration Protocol) server. When a device connects to a network, it sends a request to the DHCP server, which assigns an available IP address to the device. The IP address may change each time the device connects to the network, or after a certain period of time. Dynamic IP addresses are used in most home and small business networks, as they are easy to manage and do not require manual configuration of IP addresses on individual devices.

In summary, static IP addresses provide a permanent and easily accessible address for specific devices, while dynamic IP addresses are automatically assigned and can change over time, making them easier to manage for large networks.

# DNS 

DNS (Domain Name System) is a system that translates human-readable domain names into IP addresses that machines can understand. It is a distributed database that maps domain names to IP addresses and is used by applications, such as web browsers, to locate and access resources on the Internet.

When a user requests a website, their device sends a request to the DNS server to translate the domain name into an IP address. The DNS server then looks up the IP address in its database and returns the corresponding IP address to the user's device. The device can then use the IP address to establish a connection with the website's server and retrieve the web page.

DNS servers form a hierarchical network, with root DNS servers at the top and authoritative DNS servers for specific domains at the bottom. This allows for efficient and decentralized management of the domain name space, and ensures that all devices on the Internet can access the same information about domain names and their corresponding IP addresses.

# NAT
NAT (Network Address Translation) is a technique used to map one IP address space into another and it is commonly used to allow hosts on a private network to communicate with the Internet. NAT operates by modifying network address information in the IP header of packets, which enables the internal network to use private addresses while still allowing them to access the Internet.
There are 2 main types, SNAT and DNAT (Static and Dynamic respectively). And the preferred method uses PAT (Port Address Translation).