# EIGRP

**Définition statique des voisinages (seulement pour lien non multicast - Serie)**

`neighbor <adresse voisin> <interface>`

**Suppress routing updates on an interface**

`passive-interface fastEthernet 0/0`

**Advertise summary routes to other EIGRP routers**

`auto-summary`

**Redistribute static route**

`redistribute static`

**Exemple**

`router eigrp 1
network 1.0.0.0
network 172.16.0.0
network 192.168.2.0
network 192.168.12.0`
