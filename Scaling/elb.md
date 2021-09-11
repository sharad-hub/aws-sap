# Application load balancer Architecture

![](../images/2021-08-31-08-21-11.png)

![](../images/2021-08-31-08-26-44.png)

## Cross zone load balancing

![](../images/2021-08-31-08-32-26.png)

## ALB - Keypoints
![](../images/2021-08-31-08-36-04.png)


## SEssion state


# ELB 

### v1 =>  Classic load balancer

1 SSL cert for 1 CLB
lacking features (http)
SNI is not supported


V2- > faster, cheaper, supports target groups and rules

### ALB 
V2
HTTP/S/Websockets


### NLB

V2
TCP | TLS | UDP


Rules are processed in the order ( default one is processed at the end_)
![](../images/2021-09-01-06-41-12.png)
![](../images/2021-09-01-06-40-34.png)

![](../images/2021-09-01-06-45-38.png)

![](../images/2021-09-01-06-50-51.png)

![](../images/2021-09-01-06-52-19.png)

![](../images/2021-09-01-06-58-45.png)