# RIP

**Configure RIP**

```jsx
router rip
*! advertising network 172.30.0.0*
network 172.30.0.0
```

**Disable sending RIPv1 updates out that interface**

`passive-interface fastethernet 0/0`

**Send default static route information**

`default-information originate`

**Verify**

`show ip route`

`show ip protocols`

`debug ip rip`
