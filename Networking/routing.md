## BGP - Border Gateway Protocol

* Autonomus System (AS)- Routers controlled by one entity .. a network in BGP.
* ASN are unique and allocated by IANA ( 0- 65535), 64512- 65534 are private
* BGP Operates over tcp/179 - its reliable
* peering is manually configured
* BGP is a path vector protocol it exchanges the best path to a destination between peers .. this path is called ASPATH.
* 


* iBGP = Interal BGP - Routing within am AS ( Autonomous System)
* eBGP = External BGP - Routing between AS's

## Advance VPC routing
* Subnets are associated with 1 RT only
* Either the VPC Main RT or custom RT ( if you remove the custom RT, it will again be asociated with main RT)
* RT can also be assocaited with an IGW and VGW
* IPv4 and IPv6 handled separately within a RT
* Routes send traffic based on destination to a target
* 50 RT and 100 RT ( --- Limits)
* All Routes are evaluated- highest priority matching is used


### Routing priority orders
* Longest prefix wins
* Static Routes
* Propagated Routes

* DX
* VPN Static
* VPN BGP
* AS_Path  (shortest AS path will win)

![](../images/2021-08-25-08-39-42.png)