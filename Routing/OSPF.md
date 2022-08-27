# OSPF

Only the DR and BDR listen for 224.0.0.6

The DR uses the multicast IPv4 address 224.0.0.5 which is meant for all OSPF routers

The DR then sends out the LSA to all OSPF routers using the multicast IPv4 address 224.0.0.5

OSPFv2 Hello packets are transmitted to multicast address 224.0.0.5 (all OSPF routers) every 10 seconds

[OSPF STATES](https://www.notion.so/57cc8f4cb99c4468a17c8c96589a5646)

## OSPF Commands

```jsx
router ospf 10
router-id 2.2.2.2
```

**Configure OSPF using the network command**

based on network

`network 10.10.1.0 0.0.0.255 area 0`

based on interface

`network 10.10.1.1 0.0.0.0 area 0`

**Configure OSPF directly on the interface**

```jsx
interface GigabitEthernet 0/0/0
ip ospf 10 area 0
```

**Configure passive interfaces**

enable for lo0

`passive-interface loopback 0`

disable for g0/0/0

`no passive-inteface g0/0/0`

enable for all interface

`passive-interface default`

**Enable OSPF Point-To-Point Networks**

```jsx
interface GigabitEthernet 0/0/0
ip ospf network point-to-point
```

**Configure OSPF Priority**

```jsx
interface GigabitEthernet 0/0/0
ip ospf priority 255
```

**Clear OSPF process**

`clear ip ospf process`

**Adjust the reference bandwidth**

`auto-cost reference-bandwidth *Mbps*`

*Cost = reference bandwidth / interface bandwidth*

**Set the cost value for the loopback interface to 10**

```jsx
interface lo0
ip ospf cost 10
```

**Modify OSPFv2 Intervals**

```jsx
ip ospf hello-interval *seconds*
ip ospf dead-interval *seconds*
```

**Propagate a Default Static Route in OSPFv2**

`default-information originate`

**Summarizing OSPF routes**

```jsx
router ospf 1
area 1 range 192.168.0.0 255.255.0.0
```

**Verify**

`show ip protocols`

`show ip ospf interface brief`

`show run | begin router ospf`

check ospf state

`show ip ospf interface Gi0/0`

monitor the DR and BDR election process

`debug ip ospf adj`
