# Redistributing routes

**Redistributing OSPFv2 routes into EIGRP Routing Domain**

`router eigrp 100`

`redistribute ospf 10 metric 1500 100 255 1 1500`

**Verify**

`show ip route`

**Redistributing EIGRP Routes into OSPFv2 Routing Domain**

`router ospf 10`

`redistribute eigrp 100 subnets`

**As External Type 1 Routes**

`redistribute eigrp 100 subnets metric-type 1 subnets`

**Distribute Lists**

Configuring Distribute Lists

IN

router ospf 10

distribute-list ROUTE-FILTER in Ethernet 0/0

OUT

Creation ACL ROUTE-FILTER

router ospf 10

distribute-list ROUTE-FILTER out eigrp 100

**Prefix Lists**

Configuring Prefix Lists

ip prefix-list 

**Routes map**
