# Transit Gateway

* Network transit Hib to connect VPCs to an on premise network
* Significantly reduces network complexity
* Single network object - HA and Scalable
* Attachments to other network types
* VPC, site to site VPN & Direct Connect Gateway


## Network without Transit gateway

![](../images/2021-08-25-08-18-24.png)



## Network with transit gateway
![](../images/2021-08-25-08-13-03.png)

* Support transit routing
* Can be used to create Global networks
* Share between accounts using AWS RAM
* Peer with different regions - (same or cross account)
* Less complexity vs w/o TGW