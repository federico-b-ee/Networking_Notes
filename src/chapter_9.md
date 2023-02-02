# Protocols

A network protocol is a set of rules and standards that govern the communication between devices on a network. These protocols specify the format and structure of the data being transmitted, as well as the methods and procedures for transmitting, receiving, and processing that data. Examples of common network protocols include TCP/IP, HTTP, FTP, SMTP, and DNS.

# (ARP) Address Resolution Protocol
Network protocol used to map an IP address to a physical (MAC) address on a local network. ARP maintains a cache (table) of mappings, which helps reduce the amount of broadcasts necessary for determining the physical address associated with an IP address. Works at layer 2.

IPv6 doesn't use ARP (Address Resolution Protocol) because ARP was designed for IPv4 and its 32-bit address space. IPv6 has a larger 128-bit address space and uses a different mechanism, called Neighbor Discovery (ND), to resolve addresses to physical addresses. ND provides additional features compared to ARP, such as router discovery and address auto-configuration.