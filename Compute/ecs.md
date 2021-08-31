# ECS

## Container Definition
- Task definition
- Task Role ( to access AWS Services)
- A Task can contain one or more containers

* Image & Port
### Task Definition
- SEcurity (TAsk Role)
- Containers (s),
- Resources

[Task Role]: IAM Role which the task assumes
[Service]: How many copies, HA, Restarts


### Service Defintion
- To Configure load distribution
- Configure load balancer
- Used for scalibility and high availability



### ECS Cluster Type

#### EC2 Mode

![](../images/2021-08-30-08-08-47.png)

- Number of EC2 running (user manages )
- Have to pay even if containers are not running


#### Fargate Mode

![](../images/2021-08-30-08-14-35.png)


- Small / Burst workload -Fargate mode
- Batch /Periodic workload -Fargate mode

- Large workload - overhead conscious  -Fargate mode
= Large workload - price conscious - EC2 mode