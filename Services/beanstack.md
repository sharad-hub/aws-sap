![](../images/2021-09-21-06-52-25.png)

## Deployment policy
 ![](../images/2021-09-21-07-10-24.png)

#### All at once
 ![](../images/2021-09-21-07-11-28.png)

#### Rolling
![](../images/2021-09-21-07-12-21.png)

#### Rolling with additional batches
![](../images/2021-09-21-07-14-24.png)

#### Immutable
![](../images/2021-09-21-07-15-46.png)

#### Traffic splitting
![](../images/2021-09-21-07-16-37.png)

#### Blue green
![](../images/2021-09-21-07-17-30.png)

#### Elasticbeanstack and RDS
![](../images/2021-09-21-07-21-30.png)

![](../images/2021-09-21-07-23-17.png)

#### ebextensions
You can add AWS Elastic Beanstalk configuration files (.ebextensions) to your web application's source code to configure your environment and customize the AWS resources that it contains. Configuration files are YAML- or JSON-formatted documents with a .config file extension that you place in a folder named .ebextensions and deploy in your application source bundle.

https://github.com/awsdocs/elastic-beanstalk-samples/tree/master/configuration-files

![](../images/2021-09-21-07-26-17.png)

##  Elastic Beanstalk and HTTPS
![](../images/2021-09-21-07-27-46.png)

## EB Cloning
You can use an existing Elastic Beanstalk environment as the basis for a new environment by cloning the existing environment. For example, you might want to create a clone so that you can use a newer version of the platform branch used by the original environment's platform. Elastic Beanstalk configures the clone with the same environment settings used by the original environment. By cloning an existing environment instead of creating a new environment, you don't have to manually configure option settings, environment variables, and other settings. Elastic Beanstalk also creates a copy of any AWS resource associated with the original environment. However, during the cloning process, Elastic Beanstalk doesn't copy data from Amazon RDS to the clone. After you create the clone environment, you can modify environment configuration settings as needed.
![](../images/2021-09-21-07-30-25.png)

## EB and Docker 
AWS Elastic Beanstalk can launch Docker environments by building an image described in a Dockerfile or pulling a remote Docker image. If you're deploying a remote Docker image, you don't need to include a Dockerfile. Instead, if you are also using Docker Compose, use a docker-compose.yml file, which specifies an image to use and additional configuration options. If you are not using Docker Compose with your Docker environments, use a Dockerrun.aws.json file instead.
![](../images/2021-09-21-07-33-37.png)
![](../images/2021-09-21-07-34-45.png)