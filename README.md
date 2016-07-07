# TCP/IP Questions

## Questions

### CloudFlare "Interview Questions"
```
Q: What is the lowest TCP port number?
```
```
Q: The TCP frame has an URG pointer field, when is it used?
```
```
Q: Can the RST packet have a payload?
```
```
Q: When is the "flow" field in IPv6 used?
```
```
Q: What does the IP_FREEBIND socket option do?
```
```
Q: What does the PSH flag actually do?
```
```
Q: The TCP timestamp is implicated in SYN cookies. How?
```
```
Q: Can a "UDP" packet have a checksum field set to zero?
```
```
Q: How does TCP simultaneous open work? Does it actually work?
```
```
Q: What is a stupid window syndrome?
```
```
Q: What are the CWE and ECE flags in TCP header?
```
```
Q: What is the IP ID field and what does it have to do with DF bit? Why do some packets have a non-zero IP ID and a DF set?
```
```
Q: Can a SYN packet have a payload? (hint: new RFC proposals)
```
```
Q: Can a SYN+ACK packet have a payload?
```
```
Q: ICMP packet-too-big messages are returned by routers and contain a part of the original packet in the payload. What is the minimal length of this payload that is accepted by Linux?
```
```
Q: When an ICMP packet-too-big message is returned by an intermediate router it will have the source IP of that router. In practice though, we often see a source IP of the ICMP message to be identical to the destination IP of the original packet. Why could that happen?
Linux Configuration
```
```
Q: Linux has a "tcp_no_metrics_save" sysctl setting. What does it save and for how long?
```
```
Q: Linux uses two queues to handle incoming TCP connections: the SYN queue and the accept queue. What is the length of the SYN queue?
```
```
Q: What happens if the SYN queue grows too large and overflows?
```
```
Q: What are BGP bogons, and why are they less of a problem now?
```
```
Q: TCP has an extension which adds MD5 checksums to packets. When is it useful?
```
```
Q: What are the differences in checksumming algorithms in IPv4 and IPv6?
```

### The TCP/IP Drinking Game
```
Q: What is a fuzzball router?
A: The first modern router on the Internet, used on the first 56KB/sec NSFnet (1980s).
```
```
Q: What is a pure ACK?
A: An ACK packet that has no data.
```
```
Q: Which was possibly one of the earliest remote DoS attacks?
A: +++ATH hangup (usually inside an ICMP echo request) from the Hayes command set used by first modems.
```
```
Q: What is a Bogon packet?
A: An IP packet having a source IP of a private address space but appearing on the public internet.
```
```
Q: Which L3 protocol is used along with multicasting?
A: IGMP (Internet Group Message Protocol)
```
```
Q: What is the RFC for TCP Congestion Control?
A: RFC 2581
```
```
Q: What does EOL mean in TCP context?
A: End-of-options-list which can also be used as padding.
```
```
Q: How many bytes will a TCP header be when the Timestamp option is included?
A: 32 bytes (20 bytes minimum header + 10 bytes Timestamp + 2 bytes padding).
```
```
Q: Which is the only IP header field that cannot be manipulated with a raw socket on Linux?
A: IP total length
```
```
Q: What is the main technique used by PortBunny?
A: Sending 'trigger packets' of variable size to find optimal delay value.
```
```
Q: Who is the creator of p0f?
A: Michal Zalewski aka lcamtuf
```
```
Q: What is IPoAC?
A: IP over Avian Carriers, RFC 1149, issued on April 1, 1990.
```
```
Q: Name one technique that Nmap doesn't use for OS fingerprinting?
A: Passive OS fingerprinting, since it would be less accurate.
```
```
Q: Who were the inventors of SYN cookies?
A: Phil Karn and D.J. Bernstein aka djb
```
```
Q: Which Linux kernel developer maintains the SKB diet page?
A: Dave S. Miller
```
```
Q: Which Nmap option invokes the RPC grinder?
A: -sR
```
```
Q: Who is the creator of hping2?
A: Salvatore Sanfilippo aka antirez
```
```
Q: What kind of probes does pakketto keiretsu's paratrace use?
A: TCP Keepalive probes
```
```
Q: What is TCP piggybacking?
A: Placing data inside an ACK packet.
```
```
Q: Which TCP Timer can potentially be reset infinitely?
A: The TCP Persist Timer
```
```
Q: What is the slow start initial threshold (ssthresh) size?
A: 65535 bytes
```
```
Q: What is the main problem of NewReno?
A: It doesn't scale well.
```
```
Q: Which hosts are vulnerable to being leveraged in a zombie scan attack?
A: Any network stack implementation that uses predictable IP IDs.
```
```
Q: What is the use of the TCP_DEFER_ACCEPT option?
A: The kernel does not inform the listening socket of a new connection until the client has sent both the last ACK packet of the 3way handshake and some initial data.
```
```
Q: Which are the basic timers that TCP uses?
A: Connection Establishment, Retransmission, Delayed ACK, Persist, Keepalive, FIN_WAIT_2 and TIME_WAIT(2MSL)
```
```
Q: Name an attack that can lead to network congestion collapse.
A: Fake duplicate ACKs
```
```
Q: What is the default congestion avoidance algorithm since Linux 2.6.19?
A: CUBIC -> cat /proc/sys/net/ipv4/tcp_congestion_control: cubic
```
```
Q: What is the maximum RTO on Linux?
A: 2 minutes -> include/net/tcp.h: #define TCP_RTO_MAX ((unsigned)(120*HZ))
```

### The TCP/IP Drinking Game
```
Q: What should happen upon receipt of a RST packet containing data?
A: The host should accept it. It was suggested that a RST could contain ASCII text explaining the error, but no standard was ever established.
```
```
Q: What is the longest acceptable delay for an ACK?
A: 0.5 seconds.
```
```
Q: An ICMP error message must include what data from the original erring datagram?
A: The IP header and at least 8 bytes of payload.
```
```
Q: What is the major difference between Windows tracert and Van Jacobson-style UNIX traceroute?
A: Windows tracert uses ICMP where Van Jacobson-style traceroute uses UDP.
```
```
Q: Name three modern OS's that still use the mbuf structure, described in detail in TCP/IP Illustrated.
A: FreeBSD, OpenBSD, NetBSD
```
```
Q: What is cheapernet?
A: Coaxial cable with a diameter no longer suited to hit burglers with. The original ethernet cables were 1/2" in diameter and quite rigid.
```
```
Q: How many colours are in an 8-wire Cat5 cable?
A: Four. The other four wires are colour/white striped.
```
```
Q: What are the four colours in Cat5 cables?
A: Orange, Blue, Brown, Green
```
```
Q: How does a Windows machine react if ports above 1080 are blocked by a router?
A: A regular user can surf for roughly 2min after booting, then has to reboot.
```
```
Q: What happens if a network card's transmit interrupts are blocked in Linux?
A: Usually nothing. But on packet loss, retransmits can get delayed indefinitely.
```
```
Q: Who wrote the original Ping program?
A: Mike Muuss
```
```
Q: What's the base UDP port number used in the original Traceroute program?
A: 33434 (32768 + 666)
```
```
Q: What's the minimum value allowed for the Header Length field in a valid IPv4 header?
A: 5 (5 * 4 = 20)
```
```
Q: Which RFC introduced the TCP Timestamps option?
A: RFC 1323
```
```
Q: While computing the checksum of a TCP packet, what happens to the checksum?
A: It's replaced (or filled) with zeros.
```
```
Q: What is the Ethernet type for the Banyan Vines protocol?
A: 0BAD
```
```
Q: Name at least two colors of packet-dropping mechanism that are NOT an acronym or an abbreviation.
A: BLUE, GREEN, PURPLE, WHITE (RED and BLACK are acronyms).
```
```
Q: What was PC-IP?
A: The first implementation of TCP/IP on an IBM PC.
```
```
Q: What semi-famous hacker tool uses port 31337?
A: Back Orifice, from Cult of the Dead Cow.
```
```
Q: What two ICMP types should never be blocked?
A: ICMP type 3, Destination Unreachable, especially code 4, "fragmentation needed but don't fragment bit set" (necessary for path MTU discovery) and ICMP type 11, time exceeded (so you can use traceroute from inside the network and get replies).
```
```
Q: What is the typical MTU for an RFC 1149 transmission?
A: From RFC 1149, Carrier Pigeon Internet Protocol: "The MTU is variable, and paradoxically, generally increases with increased carrier age. A typicall MTU is 256 milligrams"
```
```
Q: What data link layer algorithm is described by an "algorhyme" in the original paper? Extra credit for reciting the first two lines.
A: The spanning tree algorithm by Dr. Radia Perlman
A: The first two lines are: I think that I shall never see / A graph more lovely than a tree.
```
```
Q: What is the minimum length of an Ethernet packet, and why is there a minimum length?
A: 64 bytes. It must be this long so that a collision can be detected.
```
```
Q: What is the 'Stretch ACK violation' documented in RFC 2525?
A: When using delayed ACKs, the receiver sends an ACK less frequently than every other sender's MSS causing potential performance degradation.
```
```
Q: Name at least three official DNS resource record types.
A: Any three of A, CNAME, HINFO, MX, NS, PTR, SOA, TXT, WKS, RT, NULL, AXFR, MAILB, MAILA, KX, KEY, SIG, NXT, PX, NSAP, NSAP-PTR, RP, AFSDB, RT, GPOS, DNAME, AAAA, SRV, LOC, EID, NIMLOC, ATMA, NAPTR, CERT, SINK, OPT, APL, TKEY, TSIG, IXFR, Deprecated: MB, MD, MF, Experimental: MINFO, MR, MG, X25
```
```
Q: What is the maximum amount of data in a UDP packet over IPv6?
A: 65487 bytes (65535 - 40 IPv6 header - 8 UDP header).
```
```
Q: What is the minimum IPv6 datagram size that a host must be able to receive?
A: 1280 bytes.
```
```
Q: What is the IANA reserved Ethernet MAC address range for IP Multicast?
A: 01:00:5e.
```
```
Q: Name one of the Ethernet patent (#4,063,220) holders.
A: Robert Metcalfe, David Boggs, Charles Thacker, or Butler Lampson. (Metcalfe and Lampson are generally credited for the invention.)
```
```
Q: What is the MAC address prefix for DECnet addresses?
A: AA:00:04:00
```
```
Q: Who wrote the original traceroute program?
A: Van Jacobson
```
```
Q: What feature of IP is central to most traceroute implementations?
A: The TTL (Time To Live) field. Most traceroutes send packets with artificially small TTLs and use the ICMP Time Exceeded responses from intermediate hosts to trace the route to a host.
```
```
Q: Why was traceroute originally implemented using UDP packets rather than ICMP echo requests?
A: In 1988, many TCP/IP stacks didn't return ICMP Time Exceeded responses to ICMP packets, but would for UDP packets.
```
```
Q: What is RED, Random Early Detection?
A: A route queuing protocol used for congestion avoidance. Once it detects "incipient congestion," the router randomly discards packets based on average queue size.
```
```
Q: What application uses TCP port 666?
A: Doom.
```
```
Q: What is "ships in the night" routing?
A: When you run two or more routing protocols on the same router.
```
```
Q: What does CRC stand for?
A: Cyclic Redundancy Check.
```
```
Q: What IP network is reserved for internal testing?
A: Anything with a netid (first octet) of 127.
```
```
Q: What are class D networks used for?
A: Multicasting.
```
```
Q: What is bootp an abbreviation for?
A: Bootstrap protocol.
```
```
Q: What is a runt packet?
A: A packet that is shorter than the minimum packet length as defined by the protocol it is using.
```
```
Q: As of RFC 1394, how many values can the TOS field in an IPv4 header have?
A: 5 (4 bit wide field, only one may be set at a time, 0 is valid).
```
```
Q: What is the H.323 protocol used for?
A: Video or teleconferencing ("Packet-based multimedia communications systems").
```
```
Q: What OSI model layer does IP most closely resemble?
A: The network layer, layer 3.
```
```
Q: Why do IP packets have a TTL (Time To Live) field?
A: To prevent a packet being retransmitted forever in the case of a routing loop.
```
```
Q: What experimental protocol might be able to fulfill RFC 1122's requirement of "SHOULD: able to leap tall buildings at a single bound?"
A: CPIP, Carrier Pigeon Internet Protocol.
```
```
Q: What are the Dave Clark Five?
A: RFCs 813 through 817.
```
```
Q: What was the first remotely operated non-computer appliance to be connected to the Internet?
A: A toaster (controlled using SNMP).
```
```
Q: What is CPIP?
A: Carrier Pigeon Internet Protocol (see RFC 1149).
```
```
Q: What common multicast group uses the address 224.0.1.1?
A: NTP (Network Time Protocol).
```
```
Q: What is the only field that is different between a regular ARP packet and a gratuitous ARP packet?
A: The target IP.
```
```
Q: What error is returned if a UDP datagram is received and has a checksum error?
A: None. It is silently discarded.
```
```
Q: What is the minimum IP datagram size that a host must be able to receive?
A: 576 bytes.
```
```
Q: When is the transmitted UDP checksum 0?
A: When the sender did not compute it.
```
```
Q: Which is the only field used twice in the UDP checksum calculation?
A: UDP length.
```
```
Q: Why is a pad byte of 0 occasionally appended for the UDP checksum calculation?
A: Because the checksum algorithm requires an even number of bytes.
```
```
Q: What are the 5 fields of a UDP pseudoheader?
A: Source IP, destination IP, zero, protocol, UDP length.
```
```
Q: Which parts of the packet does the UDP checksum cover?
A: UDP pseudoheader, UDP header, UDP data.
```
```
Q: Which parts of the packet does the IP checksum cover?
A: The IP header.
```
```
Q: What is the maximum amount of data in a UDP packet over IPv4?
A: 65507 bytes (65535 - 20 IP header - 8 UDP header).
```
```
Q: Who was the first individual member of the Internet Society?
A: Jon Postel, narrowly beating Steve Wolff.
```
```
Q: Why hasn't RFC 1149 been ratified?
Hint: RFC 1149 specifies an unusual encapsulation of IP.
A: The Avian Transmission Protocol has only been implemented once so far : http://www.blug.linux.no/rfc1149/
```
```
Q: How many identical acks need to be received for fast retransmit to occur?
A: 4 (3 duplicate + original).
```
```
Q: Under what circumstances is the TCP checksum incorrect, on a well-formed, in-flight packet?
A: When the packet is using the IP source routing option (the destination IP changes along the route, which is used to calculate the TCP checksum).
```
```
Q: How many bytes total are in a standard sized ICMP echo request packet?
A: 84 bytes (56 data, 8 ICMP header, 20 IP header).
```
```
Q: What does "IETF" stand for?
A: Internet Engineering Task Force.
```
```
Q: What does SLIP stand for?
A: Serial Line Internet Protocol.
```
```
Q: What is the TCP retransmission ambiguity problem?
A: An ACK arrives after a retransmit - was it sent in response to the initial transmit or the retransmit?
```
```
Q: Name one way to solve the TCP retransmission ambiguity problem.
A: Use the Eifel detection algorithm.
A: Enable timestamps (which is what Eifel does).
```
```
Q: When is an IGMP report timer cancelled?
A: When the host receives an IGMP report for the same group (with a matching destination IP).
A: When more than one host is a member of the same group on the same network.
```
```
Q: How many bits are in an "A" type DNS resource record?
A: 112, plus the owner name.
```
```
Q: What is archived at www.kohala.com?
A: Richard Stevens' website.
```
```
Q: What does the tcp_close_wait_interval configuration option really do in Solaris?
A: Sets the duration of the TIME_WAIT state.
```
```
Q: What is the range of class B IP addresses?
A: 128.0.0.0 through 191.255.255.255.
```
```
Q: What is the significance in networking of the amateur radio callsign KA9Q?
A: It's the callsign of Phil Karn, who worked on SLIP, congestion control and TCP over amateur radio.
```
```
Q: Sally Floyd was heavily involved in the design of which TCP enhancement?
A: ECN, see RFC 3042.
```
```
Q: Who said: "The IETF already has more than enough RFCs that codify the obvious, make stupidity illegal, support truth, justice, and the IETF way, and generally demonstrate the author is a brilliant and valuable Contributor to The Standards Process"?
A: Vernon Schryver, on the mailing list for the tcp-impl IETF working group.
```
```
Q: What is the minimum MTU that allows any IP datagram to pass?
A: 68 bytes.
```
```
Q: What is a syncookie and who invented it?
A: Syn cookies help avert synflood attacks by forcing all of the TCP state into the client, invented by Dan Bernstein.
```
```
Q: Van Jacobson claimed that the TCP receive packet processing fast-path could be done in how many instructions?
A: 30. (33 on Sparc, due to "compiler brain damage.")
```
```
Q: What would happen if you implemented the TCP URG pointer according to the standard?
Hint: RFC 1122 cleared up the confusion generated by RFC 793.
A: You would lose the last byte of urgent data because the other host implements BSD-style urgent pointers, which point to the byte following the last byte of urgent data.
```
```
Q: What is an LFN (spelled L-F-N, pronounced "elephant")?
A: Long Fat Network, defined in RFC 1072.
```
```
Q: Where was John Nagle working when he invented the "Nagle algorithm?"
A: Ford Motor Company.
```
```
Q: Who invented Tinygram Avoidance?
A: John Nagle. (Tinygram Avoidance is also known as the "Nagle algorithm.")
```
```
Q: What is the sub-group FHE within the IETF?
A: Facial hairius extremis, spotted at IETF conferences and noted in RFC 2323, "IETF Identification and Security Guidelines."
```
```
Q: Under what circumstances should you return error number 418: "I'm a teapot"?
A: Any attempt to brew coffee with a teapot according to RFC 2324, "Hyper Text Coffee Pot Control Protocol."
```
```
Q: Who found additional problems beyond those in RFC 1337, "TIME-WAIT Assassination Hazards in TCP" which have yet (as of Feb 2002) to be fixed?
Hint: He died after publishing the initial draft.
A: Ian Heavens
```
```
Q: Private networks came from RFC 1597. Which later RFC claims this is a bad idea?
A: RFC 1627, "Network 10 Considered Harmful."
```
```
Q: What makes it very difficult for any network stack to claim "strict compliance" to RFC 1122?
A: Its requirement of "SHOULD: able to leap tall buildings at a single bound."
```
```
Q: Who said "If you know what you are doing, three layers is enough; if you don't even seventeen levels won't help?"
A: Mike Padlipsky (or MAP).
```
```
Q: Which OSI networking model layers do TCP and IP correspond to?
A: They don't. (Any answer with any kind of equivocation should be accepted.)
```
```
Q: Who invented NAT (Network Address Translation)?
A: Paul Francis (but he credits Van Jacobson for the concept).
```
```
Q: How many hosts should be on a network with a 255.255.255.192 subnet mask?
A: 62 (64 - (broadcast address and network address))
```
```
Q: How many bytes are in an IPv4 header without options?
A: 20.
```
```
Q: Name one of the men described as "The Father of the Internet."
A: Any of: Vinton Cerf (TCP/IP co-designer), Robert Kahn (TCP/IP co-designer), John Postel (started IANA), Al Gore (made encouraging noises)
```
```
Q: What does TCP/IP stand for?
A: Transmission Control Protocol/Internet Protocol.
```
```
Q: How many layers are in the OSI networking model?
A: 7.
```
```
Q: Name a network address designated for private network use.
A: 10.0.0.0, 192.168.0.0, or 172.16.0.0
```
```
Q: Name two TCP header options.
A: Any 2 of maximum segment size (MSS), window scale factor, timestamp, noop, SACK, and end of options list.
```
```
Q: What is the MSL as defined in RFC 793?
A: 2 minutes (but is usually implemented as 30 seconds).
```
```
Q: Name two ways to exit the TIME_WAIT state.
A: 2MSL timeout, TIME_WAIT assassination (receive a RST), or receive a SYN with greater sequence number. Note: TIME_WAIT assassination is not permitted by RFC 1337.
```
```
Q: What is the TCP state that can only be reached through a simultaneous close?
A: CLOSING
```
```
Q: What year was the first IETF meeting held?
A: 1986.
```
```
Q: Name all 7 layers of the OSI network model.
A: Physical, Data Link, Network, Transport, Session, Presentation, and Application.
```
```
Q: Why are many network services assigned odd ports?
A: The precursor to TCP and UDP was NCP, which was simplex and required 2 ports for one connection. When duplex protocols arrived, the even port numbers were abandoned.
```
```
Q: Which two of these three protocols are the most similar: IPv4, IPv6, or CLNP?
A: IPv4 and CLNP. (CLNP stands for ConnectionLess Network Protocol, and is basically IPv4 with larger addresses.)
```
```
Q: In TCP, simultaneous open is a transition between which two TCP states?
A: From SYN_SENT to SYN_RCVD.
```
```
Q: What is the ICMP type field for an Echo Request?
A: 8.
```
```
Q: What is the ICMP type field for an Echo Reply?
A: 0.
```
```
Q: What is the maximum number of IP addresses recordable by the IP Record Route option?
A: 9.
```
```
Q: If one end of a TCP connection crashes, and the other end doesn't attempt to send any data, is the resultant TCP connection half-open or half-closed from the point of view of the host that's still up?
A: Half-open.
```
```
Q: In a Christmas tree packet, which TCP flag bits are turned on?
A: SYN, URG, PSH, and FIN (all of them).
```
```
Q: TCP was defined in which RFC?
A: RFC 793, "Transmission Control Protocol."
```
```
Q: What is silly window syndrome?
A: In TCP, when the receiving end continually advertises a tiny window, resulting in data being sent in very small packets.
```
```
Q: If the remote host of a TCP connection does not advertise an MSS, what is the assumed MSS?
A: 536 bytes over IPv4, 1220 over IPv6, although most implementations default to 512 and 1024 respectively.
```
```
Q: How is the initial path MTU of a TCP connection calculated?
A: min (outgoing interface MTU, remote advertised MSS)
```
```
Q: Why was the "AAAA" DNS resource record type created?
A: For IPv6 addresses.
```
```
Q: What is the maximum amount of data allowed in an IPv4 packet?
A: 65515 bytes (65535 - 20, max total length minus 20 bytes of header)
```
```
Q: What was the default send and receive buffer size in 4.3BSD?
A: 2048 bytes.
```
```
Q: In TCP, when is the sender limited by the congestion window?
A: When using the slow start algorithm, after packet loss has occurred.
```
```
Q: In most implementations of TCP, what byte does the urgent pointer point to?
A: The byte following the last byte of urgent data.
```
```
Q: What service runs on port 6667?
A: Internet Relay Chat (IRC)
```
```
Q: Name three methods or algorithms related to congestion control in TCP.
A: Congestion window, Vegas, Reno, NewReno, SACK, DSACK, FACK, Eifel algorithm, ECN, RTO
```
```
Q: The ECN field uses which bits in the byte that contains the IPv4 TOS field?
A: Bits 6 and 7.
```
```
Q: What's wrong with the standard way of estimating RTO (Retransmission TimeOut)?
A: It places too much weight on the variance of round trip times.
```
```
Q: What is the minimum data payload in a ping of death?
A: 65508 bytes (65536 - 20 IP header - 8 ICMP header)
```
```
Q: What's the MTU of HiPPI (High Performance Parallel Interface)?
A: 65280 bytes
```
```
Q: How large is an entire AAL/5 encapsulated ATM cell?
A: 53 bytes (48 data + 5 header)
```
```
Q: Distance vector and link state are two types of what kind of protocol?
A: Routing protocols
```
```
Q: The IPv4 fields formerly known as TOS (Type Of Service) and precedence are now called what?
A: The DS (Differentiated Services) and ECN (Explicit Congestion Notification) fields.
```
```
Q: Why do most traceroute implementations NOT use the IP Record Route option to find intermediate hosts?
A: The IP Record Route option can only record 9 intermediate hosts, which is too few for many routes in the modern Internet.
```
```
Q: Which spelling is correct, Van Jacobson or Van Jacobsen?
A: Van Jacobson.
```
```
Q: Who invented the spanning tree algorithm?
A: Dr. Radia Perlman
```

## Links
* [CloudFlare "Interview Questions"](https://blog.cloudflare.com/cloudflare-interview-questions/)
* [The TCP/IP Drinking Game](http://valerieaurora.org/tcpip.html)
* [TCP/IP Drinking Game](http://sock-raw.org/netsec/tcpipdrink.html)
