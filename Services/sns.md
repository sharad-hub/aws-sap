
# SNS


- Based on pub sub model
- Public AWS service - network connectivity with Public Endpoint
- Coordinates the sending and delivery of messages
- Messages are <= 256 KB

SNS Topics are the base entity of SNS - permission and configuration.
- A publisher sends message to a TOPIC
- Topics have subscribers which receives messages
HTTP(s), Email(Json), SQS, Mobile Push, SMS, Lambda functions
- SNS is used across AWS for notification (eg cloudwatch and cloudformation)

![](../images/2021-08-30-08-48-34.png)


Delivers status (including HTTP, Lambda, SQS) 
Delivery Retries - Reliable Delivery
HA and Scalable (Region)  -- all data is replicated inside a region , if a particular AZ fails, SNS will continue to work.
Server side Encryption
Cross-Account via TOPIC Policy
