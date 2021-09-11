# RDS
- Database as a service (DBaaS) more accurately as DatabaseServer as a service
- Managed Database Instances ( 1+ Databases)

### 
![](../images/2021-09-02-08-40-40.png) 

## RDS Architecture
![](../images/2021-09-02-08-44-51.png)

![](../images/2021-09-02-08-51-19.png)

## RDS Multi AZ

![](../images/2021-09-02-08-55-51.png)

Now if an error occurs with the primary instance, RDS detects this and changes the database endpoint CNAME, moving it from the primary instance across to the standby replica.
- very brief interruptions
- Typically this failover 60-120 seconds

###### RDS Multi AZ provides high availability | It DOES NOT provide fault tolerance

![](../images/2021-09-02-08-56-22.png)


### EXAM Points

- Not free tier
- Standby can't be directly used ()
- 60-120 seconds failover
- Same region only (others Azs in the same VPC)
- Backups are taken from standby ( removes performance impact)

![](../images/2021-09-02-09-36-22.png)

### RDS Backups and Restore

##### RTO vs RPO

![](../images/2021-09-03-06-37-11.png)


![](../images/2021-09-03-06-47-32.png)
![](../images/2021-09-03-07-01-01.png)

Benefit of using S3 is that, any data contained in backups is now region resilient because it's stored in S3, which replicates data across multi availability zones in that region.
RDS backup occurs from single db instance if multi az is disabled or from standby instance is multi az is enabled.

- Manual snapshots does not expire, you have to clear them up by yourself.
- incremental backup only stores changes in the data.
- Transaction logs can be used to achive RTO of 5 min, by re running the queries from the transaction logs.
- Automatic backups are releated automaticaly ( when we delete the data)
![](../images/2021-09-03-07-04-55.png)

### Read Replica

- PErformance
- Availability

- Synchronous replication -> Multi AZ
- Asynchronous replication -> Read replica
![](../images/2021-09-03-07-10-00.png)


![](../images/2021-09-03-07-13-27.png)
![](../images/2021-09-03-07-16-02.png)


#### RDS Security
![](../images/2021-09-03-07-20-48.png)
![](../images/2021-09-03-07-22-42.png)

![](../images/2021-09-03-07-29-20.png)