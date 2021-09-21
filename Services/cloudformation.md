
AWS CloudFormation provides several built-in functions that help you manage your stacks. Use intrinsic functions in your templates to assign values to properties that are not available until runtime.

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html

![](../images/2021-09-19-08-14-38.png)

![](../images/2021-09-19-08-17-18.png)
![](../images/2021-09-19-08-20-09.png)
![](../images/2021-09-19-08-21-32.png)
![](../images/2021-09-19-08-23-11.png)
![](../images/2021-09-19-08-25-00.png)

## Cloudformation Mappings
![](../images/2021-09-19-08-28-28.png)

## Cloudformation Outputs
![](../images/2021-09-19-08-31-53.png)

## Cloudformation Conditions
The optional Conditions section contains statements that define the circumstances under which entities are created or configured. You might use conditions when you want to reuse a template that can create resources in different contexts, such as a test environment versus a production environment. In your template, you can add an EnvironmentType input parameter, which accepts either prod or test as inputs. Conditions are evaluated based on predefined pseudo parameters or input parameter values that you specify when you create or update a stack. Within each condition, you can reference another condition, a parameter value, or a mapping. After you define all your conditions, you can associate them with resources and resource properties in the Resources and Outputs sections of a template

## Depends On
With the DependsOn attribute you can specify that the creation of a specific resource follows another. When you add a DependsOn attribute to a resource, that resource is created only after the creation of the resource specified in theDependsOn attribute.
![](../images/2021-09-19-11-01-36.png)

## CreationPolicy, WaitConditions and cfn-signal
CreationPolicy, WaitConditions and cfn-signal can all be used together to prevent the status if a resource from reaching create complete until AWS CloudFormation receives a specified number of success signals or the timeout period is exceeded.The cfn-signal helper script signals AWS CloudFormation to indicate whether Amazon EC2 instances have been successfully created or updated.

## Nested Stack
Nested stacks allow for a hierarchy of related templates to be combined to form a single product
A root stack can contain and create nested stacks .. each of which can be passed parameters and provide back outputs.
Nested stacks should be used when the resources being provisioned share a lifecycle and are related.
![](../images/2021-09-19-13-44-55.png)
![](../images/2021-09-19-13-44-12.png)

## Cross stack references
Cross stack references allow one stack to reference another
Outputs in one stack reference logical resources or attributes in that stack
They can be exported, and then using the !ImportValue intrinsic function, referenced from another stack.
![](../images/2021-09-19-13-49-29.png)
![](../images/2021-09-19-13-52-31.png)

## Stack set
StackSets are a feature of CloudFormation allowing infrastructure to be deployed and managed across multiple regions and multiple accounts from a single location.

Additionally it adds a dynamic architecture - allowing automatic operations based on accounts being added or removed from the scope of a StackSet.
![](../images/2021-09-19-13-55-52.png)
![](../images/2021-09-19-14-00-13.png)

## Deletion policy
With the DeletionPolicy attribute you can preserve or (in some cases) backup a resource when its stack is deleted. You specify a DeletionPolicy attribute for each resource that you want to control. If a resource has no DeletionPolicy attribute, AWS CloudFormation deletes the resource by default.
![](../images/2021-09-19-14-03-15.png)
![](../images/2021-09-19-14-04-25.png)

## CFN Stack Role

![](../images/2021-09-19-14-06-24.png)
![](../images/2021-09-19-14-19-52.png)

## CloudFormationInit
CloudFormationInit and cfn-init are tools which allow a desired state configuration management system to be implemented within CloudFormation

Use the AWS::CloudFormation::Init type to include metadata on an Amazon EC2 instance for the cfn-init helper script. If your template calls the cfn-init script, the script looks for resource metadata rooted in the AWS::CloudFormation::Init metadata key. cfn-init supports all metadata types for Linux systems & It supports some metadata types for Windows
![](../images/2021-09-19-14-21-40.png)
![](../images/2021-09-19-14-24-38.png)

## CFN-HUB
The cfn-hup helper is a daemon that detects changes in resource metadata and runs user-specified actions when a change is detected. This allows you to make configuration updates on your running Amazon EC2 instances through the UpdateStack API action.
![](../images/2021-09-19-14-27-54.png)

## CFN Changeset
When you need to update a stack, understanding how your changes will affect running resources before you implement them can help you update stacks with confidence. Change sets allow you to preview how proposed changes to a stack might impact your running resources, for example, whether your changes will delete or replace any critical resources, AWS CloudFormation makes the changes to your stack only when you decide to execute the change set, allowing you to decide whether to proceed with your proposed changes or explore other changes by creating another change set.

## CFN Custom Resources
Custom resources enable you to write custom provisioning logic in templates that AWS CloudFormation runs anytime you create, update (if you changed the custom resource), or delete stacks

This lesson steps through the theory and architecture of Custom Resources
![](../images/2021-09-19-14-34-21.png)