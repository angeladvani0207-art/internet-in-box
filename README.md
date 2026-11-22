# Internet in a Box

An interactive, single-file simulator of how a web request crosses the internet.

## What it models
- Home router with NAT and DHCP, ISP edge, three backbone routers, DNS resolver and authoritative DNS, stateful firewall, load balancer, two web servers
- A full page load: DNS recursion, TCP handshake, TLS, HTTP, with TCP retransmits and exponential backoff
- Link-state (Dijkstra) routing that reconverges when a cable is cut
- Queues, congestion, tail drop, packet sizes and TTL
- Traceroute using ICMP Time Exceeded, DNS caching, firewall ACL on tcp/443

## Run it
Open `index.html` in any browser. No build step, no dependencies.

## Try
1. Press **Failover demo** and watch traffic reroute after a cable is cut.
2. Raise **Cross-traffic** to fill queues and cause drops.
3. Tick **Firewall denies tcp/443** and watch TLS fail.
4. Click any node to inspect it, or press **Traceroute**.

## Ideas to extend
CDN edge cache, BGP route announcements, server health checks.
