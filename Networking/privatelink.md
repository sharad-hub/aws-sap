![](../images/2021-09-09-05-22-31.png)

![](../images/2021-09-09-05-24-36.png)

# Gateway Endpoints

Gateway endpoints are a type of VPC endpoint which allow access to S3 and DynamoDB without using public addressing.

Gateway endpoints add 'prefix lists' to route table, allowing the VPC router to direct traffic flow to the public services via the gateway endpoint.
![](../images/2021-09-09-05-29-59.png)

- Without Gateway endpoint
![](../images/2021-09-09-05-32-17.png)
- With Gateway endpoint
![](../images/2021-09-09-05-35-04.png)

# Interface Endpoints
![](../images/2021-09-09-05-38-33.png)

![](../images/2021-09-09-05-41-28.png)

- Without DNS endpoint
![](../images/2021-09-09-05-44-39.png)

- With Interface endpoint
 ![](../images/2021-09-09-05-48-05.png)

 ###### VPC Endpoint Policies
 ![](../images/2021-09-09-06-00-59.png)
 ![](../images/2021-09-09-06-02-46.png)

 ![](../images/2021-09-09-06-04-09.png)

 ![](../images/2021-09-09-06-07-33.png)