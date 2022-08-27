# STATIC

`ip route 172.31.1.0 255.255.255.128 Serial0/0/0`

directly attached static route

directly attached static route relies on its exit interface in order for packets to be sent to its destination

`ip route 172.31.0.0 255.255.255.0 172.31.1.193`

recursive static route

A recursive static route relies on the next hop router in order for packets to be sent to its destination

`ip route 172.31.0.0 255.255.255.0 s0/0/1 172.31.1.197`

fully specified route

A fully specified route is a static route that is configured with an exit

interface and the next hop address
