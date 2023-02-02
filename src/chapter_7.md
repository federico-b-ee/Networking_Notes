# Routing 

The purpose of routing is to determine the best path for data to travel from its source to its destination over a network. Routing enables the efficient and effective delivery of data by forwarding it through intermediate nodes, such as routers, to reach its final destination. Routing algorithms and protocols are used to determine the best path, taking into account factors such as network congestion, network topology, and the distance to the destination. It's a way to connect different networks.

## Routing Table
A routing table is a database that contains information about the routes and destinations of a network. The routing table is populated by routing protocols and contains information about the network's topology, including the network addresses, subnets, and metrics such as hop count and delay.

## Default Gateway

The default route or gateway is a pre-determined path for network traffic to follow when no other specific route is available. It's the last resort for routing packets and is used when a destination IP address doesn't match any other routes in the routing table. The default gateway is typically the IP address of the router that connects the local network to the internet.

## Metrics 

- Hop count: The number of routers a packet passes through from source to destination. The hop count is used as a metric in some routing algorithms.

- MTU (Maximum Transmission Unit): The largest packet size that can be transmitted over a network. The MTU affects the size of packets that can be transmitted and can impact network performance.

- Bandwidth: The amount of data that can be transmitted over a network in a given amount of time. Bandwidth is often expressed in bits per second (bps) or bytes per second (Bps).

- Latency: The time it takes for a packet to travel from source to destination. Latency is often expressed in milliseconds (ms) and is an important factor in network performance.

- Administrative Distance: Routers use administrative distance to determine which of multiple routes to the same destination to use. A lower administrative distance value indicates a more preferred route, with a default value of 0 for directly connected routes and a value of 1 for statically defined routes.

## Route Aggregation

Route aggregation refers to the process of combining multiple routing entries into a single, more specific route advertisement in order to reduce the size of routing tables and reduce the amount of network overhead. This is done by summarizing multiple routes into a single, more general route that covers all of the individual routes. This can improve network performance, reduce routing table size, and simplify network management.

## Routing Protocols

Routing protocols are used to exchange information between routers in a network to determine the best path for data to travel from source to destination. There are two main types of routing protocols:

> Distance-vector: Examples are Routing Information Protocol (RIP), Routing Information Protocol version 2 (RIPv2), and Interior Gateway Routing Protocol (IGRP).
>
> Link-state: Examples are Open Shortest Path First (OSPF) and Intermediate System-to-Intermediate System (IS-IS).

