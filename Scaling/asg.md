# Auto Scaling Group
An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management. ﻿An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
![](../images/2021-09-07-07-43-04.png)
![](../images/2021-09-07-07-44-45.png)
![](../images/2021-09-07-07-49-17.png)
![](../images/2021-09-07-07-52-54.png)
![](../images/2021-09-07-07-54-50.png)

![](../images/2021-09-07-07-56-13.png)

### ASG Lifecycle Hooks
Lifecycle hooks enable you to perform custom actions by pausing instances as an Auto Scaling group launches or terminates them. When an instance is paused, it remains in a wait state either until you complete the lifecycle action using the complete-lifecycle-action command or the CompleteLifecycleAction operation, or until the timeout period ends (one hour by default).
![](../images/2021-09-07-07-59-16.png)
![](../images/2021-09-07-08-01-50.png)