---
tags: note
status: fern
priority: 2
publish: false
aliases: 
---
**Links:** [[Network]]
# Frame
##### Definition
A small part of a message in the network, basically a container for a single network packet. Helps to identify data and determine the way it should be decoded and interpreted.

##### Questions
Frames are the units of data used in the OSI model’s **data link layer**. A frame contains more information about the transmitted message than a packet. It consists of a **header with a start of frame flag**, destination and source addresses, and data payloads.

##### Frames and packets
The main difference between a packet and a frame is that a packet is the unit of data used in the network layer, and a frame is the unit of data used in the data link layer. Also, a frame contains more information about the transmitted message than a packet.


## Related:

[[Packet]]

## Questions:
- [Q:: What you can find in header of frame ?]
- [Q:: which layer frame belongs to?]