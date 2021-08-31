

# SQS


 
- Public AWS service - network connectivity with Public Endpoint
- Highly Available
- Types: Standard and FIFO
- Coordinates the sending and delivery of messages
- Messages upto <= 256 KB in size  ( for large data link - data on s3)
- Received messages are hidden (Visibility timeout) - [if client can not delete the message in the visibility time, then it will re appear].
- DLQ can be used for problem messages

ASGs can scale and Lambda invoke based on queue length

![](../images/2021-08-30-09-02-52.png)

*Advance version*

![](../images/2021-08-30-09-05-12.png)

## FIFO
- Exactaly Once
- in order
- 3000 messages per second with batching | upto 300 without batching
- Billed based on request
- 1 request = 1- 10 messages upto 64 kb

## Standard

- At least once delivery
- Order is not maintained
- (multi level high ways) unlimited number of messages
- Billed based on request

- Short ( immediate) va Long (waittimrseconds | upto 20 seconds) polling.
- Encryption at rest (KMS) and in transit

### Standered VS FIFO

![](../images/2021-08-30-09-18-49.png)

### SQS Extended class library ( ! Important ! )

 ![](../images/2021-08-30-09-22-48.png)

 ### SQS Delay Queues ( ! Important ! )

 ![](../images/2021-08-30-09-32-48.png)

 ### DLQ

 - maxRecieveCount
 Dead letter queues allow for messages which are causing repeated processing errors to be moved into a dead letter queue in this queue, different processing methods, diagnostic methods or logging methods can be used to identity message faults.

 - Enqueue timestamp 
 ![](../images/2021-08-30-09-37-50.png)