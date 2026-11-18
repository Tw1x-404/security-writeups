# TryHackMe: Intro to Networking

Path: Pre Security

## Topic
The basics of how devices communicate in a network and how data
travels across the internet.

## Key concepts

### OSI model
A model that splits network communication into 7 layers.
Each layer has its own job:

| Layer | Name | What it does |
|---|---|---|
| 7 | Application | Interface for programs, e.g. browsers (HTTP, DNS) |
| 6 | Presentation | Data format, encoding and encryption |
| 5 | Session | Opens, manages and closes connections |
| 4 | Transport | Splits data into segments, TCP or UDP |
| 3 | Network | Routing between networks, IP addresses |
| 2 | Data Link | Communication inside a local network, MAC addresses |
| 1 | Physical | Cables, signals, the actual hardware |

### Encapsulation
When data is sent, each layer adds its own header. The receiver
removes the headers again layer by layer. That is how every layer
gets the information it needs.

### TCP vs. UDP
- TCP is reliable: it builds a connection first (three-way handshake:
  SYN, SYN/ACK, ACK) and checks that all data arrives.
- UDP is faster but does not check if data arrives. It is used for
  things like streaming or online games.

### Ports
A port tells the receiving device which service the data is for.
Common examples: 22 (SSH), 53 (DNS), 80 (HTTP), 443 (HTTPS).

## Tools I tried

| Tool | What it does |
|---|---|
| ping | Checks if a device is reachable |
| traceroute | Shows the route packets take to a target |
| whois | Shows who registered a domain |
| dig | Looks up DNS records of a domain |

## What I learned
I now understand how data is packed, sent and unpacked in a network.
This also helped me understand the SSH connections from OverTheWire
Bandit better, since SSH runs over TCP on a specific port.
