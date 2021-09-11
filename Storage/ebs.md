# EBS - General Purpose SSD (GP2)
![](../images/2021-09-07-00-04-03.png)

# EBS - General Purpose SSD (GP3)
![](../images/2021-09-07-00-07-03.png)

# EBS - Provisioned IOPS SSD (io1/2)
Provisioned IOPS SSD — Provides high performance for mission-critical, low-latency, or high-throughput workloads.
![](../images/2021-09-07-00-11-50.png)

# HDD Based 
Throughput Optimized HDD — A low-cost HDD designed for frequently accessed, throughput-intensive workloads.
Cold HDD — The lowest-cost HDD design for less frequently accessed workloads.
![](../images/2021-09-07-00-18-08.png)


# Instance store
![](../images/2021-09-07-00-26-26.png)
An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. Instance store is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.

An instance store consists of one or more instance store volumes exposed as block devices. The size of an instance store as well as the number of devices available varies by instance type.

The virtual devices for instance store volumes are ephemeral[0-23]. Instance types that support one instance store volume have ephemeral0. Instance types that support two instance store volumes have ephemeral0 and ephemeral1, and so on.
![](../images/2021-09-07-00-28-43.png)
![](../images/2021-09-07-00-30-34.png)
![](../images/2021-09-07-00-32-28.png)


### EBS vs Instance store
![](../images/2021-09-07-00-34-17.png)

![](../images/2021-09-07-00-38-21.png)