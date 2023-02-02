# IPv4

IP stands for Internet Protocol. It is a set of communication protocols used for transmitting data over the internet or other networks. IP is responsible for routing data packets between different devices on a network, and for ensuring that each packet is delivered to its intended destination.

It has two versions, IPv4 and IPv6, each with its own unique set of features and functions. IPv4 is the most widely used version, but IPv6 is gradually being adopted due to its larger address space and improved security features.

IP addresses are unique numerical labels assigned to devices on a network, and are used to identify and locate devices on the network. IP addresses, along with other network protocols, allow devices to communicate and exchange data with each other, enabling the functionality of the internet and other networks.

> IPv4 🠲 32-bit 🠲 2^32 combinations 🠲 divided in octets eg: 192.168.0.1

## Public and Private Addresses

Public IP addresses are unique, globally recognizable addresses assigned by Internet Service Providers (ISPs) to devices connected to the internet. These addresses allow devices to communicate with each other over the internet, and they are used to identify devices in website URL's and email addresses.

Private IP addresses, on the other hand, are used within private networks, such as local area networks (LANs), and are not globally unique. Private IP addresses are reserved by the Internet Assigned Numbers Authority (IANA) for use within private networks, and they are not accessible from the internet. Private IP addresses are typically assigned to devices using Dynamic Host Configuration Protocol (DHCP) and can be used for internal communication within a network.

Examples of private IP addresses are: 10.0.0.0 - 10.255.255.255, 172.16.0.0 - 172.31.255.255, and 192.168.0.0 - 192.168.255.255.

In summary, public IP addresses are used for communication over the internet, while private IP addresses are used for internal communication within a network.

## Subnet Masks

A subnet mask is used in computer networking to divide a large network into smaller subnetworks, or subnets. It works in conjunction with an IP address to define the structure of a network and the hosts within it.

A subnet mask is a 32-bit binary number that is used to determine which portion of an IP address represents the network address and which portion represents the host address. By dividing the IP address into two parts, the subnet mask allows for the creation of multiple subnets within a single network, enabling the efficient use of IP addresses and the organization of networks into smaller, more manageable units.

For example, the subnet mask 255.255.255.0 is often used in home networks to divide a network into smaller subnets. In this case, the first 24 bits of the IP address are used to represent the network address, while the remaining 8 bits are used to identify individual hosts within the network.

The use of subnet masks is a key aspect of IP networking and plays a critical role in network organization, security, and performance.

## Classes

The classes are:

> Class A: The first bit is set to 0, and the first octet ranges from 1 to 126. This class contains over 16 million IP addresses, making it suitable for large organizations and service providers.
>
> Class B: The first two bits are set to 10, and the first octet ranges from 128 to 191. This class contains over 65,000 IP addresses, making it suitable for medium-sized organizations.
>
> Class C: The first three bits are set to 110, and the first octet ranges from 192 to 223. This class contains over 256 IP addresses, making it suitable for small organizations and home networks.
>
> Class D: The first four bits are set to 1110, and the first octet ranges from 224 to 239. This class is reserved for multicast addresses.
>
> Class E: The first four bits are set to 1111, and the first octet ranges from 240 to 255. This class is reserved for future use and is not used for regular IP addresses.
> Extra: (APIPA) Automatic Private IP Addressing.

IPv4 classes were replaced by the Classless Inter-Domain Routing (CIDR) system in 1993, but the class system is still widely used in understanding and configuring IP networks.

## CIDR Notation

Classless Inter-Domain Routing (CIDR) notation is a method of representing IP addresses and subnets in a more concise and flexible format. CIDR notation replaces the traditional IP address classes (A, B, C) and subnet masks used in IPv4 addressing.

In CIDR notation, an IP address is represented as a string of numbers separated by a slash ( / ), with the number after the slash representing the network prefix length. The network prefix length determines the number of bits in the IP address that are used for the network portion and the number of bits used for the host portion.

For example, the IP address 192.168.1.0 with a subnet mask of 255.255.255.0 can be represented in CIDR notation as 192.168.1.0/24, where the number 24 represents the number of bits in the network prefix.

CIDR notation enables more efficient use of IP addresses and enables network administrators to create subnets of various sizes to accommodate different network requirements. It also provides a more flexible way to define subnets and is widely used in modern IP networking.

# IPv6

IPv6 has a much larger address space, allowing for more devices to be connected to the Internet, and also includes improved security features and a simplified header structure. IPv6 is gradually being adopted by Internet Service Providers (ISPs) and organizations, and is necessary for the continued growth of the Internet.

An example of an IPv6 address is: 2001:0db8:85a3:0000:0000:8a2e:0370:7334.

Note that IPv6 addresses are written in hexadecimal and are separated into 8 blocks of 16-bits each, separated by colons, followed by a slash and the prefix length, which represents the number of bits in the network portion of the address. The leading zeros in each block can be omitted, and consecutive blocks of zeros can be represented by a double colon (::).

2001:0db8:85a3:0000:0000:8a2e:0370:7334/64 is a valid IPv6 CIDR notation, where the prefix length is 64 bits. The prefix length determines the size of the network, and the remaining bits are used for the host portion of the address.

## Global Unicast Address

It is globally unique, assigned by the Internet Assigned Numbers Authority (IANA) or a regional Internet registry (RIR). It is used for Internet-facing devices, such as servers and routers, and is used for routing traffic across the Internet. The first three blocks of an IPv6 address are used to identify the RIR, and the next block is used to identify the specific organization.

## Local Unicast Address 

It is unique within a specific network segment, and is used for communication within a local network. The local unicast address is created using the prefix "fe80::/10" and the Interface Identifier (IID), which is derived from the MAC address of the device. The local unicast address is not globally unique, but it is unique within the local network.

In summary, the global unicast address is used for communication across the Internet, while the local unicast address is used for communication within a local network.