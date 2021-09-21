
CloudFront is a Content Delivery network (CDN) within AWS.

![](../images/This%20lesson%20steps%20through%20the%20basic%20architecture.png)
![](../images/2021-09-18-01-05-11.png)
![](../images/![](../images/2021-09-18-01-07-55.png).png)

### CloudFront Behaviours
CloudFront Behaviours control much of the TTL, protocol and privacy settings within CloudFront

### TTL and Invalidations
![](../images/2021-09-18-09-06-20.png)

![](../images/2021-09-18-09-10-44.png)
![](../images/2021-09-18-09-13-06.png)

### Cloudfront and SSL | SNI
![](../images/2021-09-18-09-18-52.png)
![](../images/2021-09-18-09-23-29.png)


![](../images/2021-09-18-09-29-03.png)

### CloudFront origins - [S3 origin | Custom origin ]
CloudFront origins store content distributed via edge locations.

The features available differ based on using S3 origins vs Custom origins

Supported SSL/TLS protocols and ciphers for communication between viewers and CloudFront

## Caching performance and Optimization
![](../images/2021-09-18-09-57-49.png)
![](../images/2021-09-18-10-08-01.png)
![](../images/2021-09-18-10-08-44.png)
###### Optimized
![](../images/2021-09-18-10-09-29.png)
![](../images/2021-09-18-10-07-39.png)

## OAI and Custom Origin
![](../images/2021-09-18-10-14-20.png)

###### OAI (origin access identity - only applicable to normal s3 | NOT to S3 Static web hosting)

![](../images/2021-09-18-10-17-49.png)

## Securing Custom Origins
![](../images/2021-09-18-10-20-19.png)

## Cloudfron Security [Private] Distribution
![](../images/2021-09-18-10-32-50.png)
![](../images/2021-09-18-10-35-23.png)
![](../images/2021-09-18-10-40-28.png)

## Cloudfront Geo Restriction
There are two common architectures for restricting access to content via CloudFront.

The build in feature set - CloudFront Geo Restriction allows for White or Black list restrictions based on ONLY Country Code

3rd Party Geolocation requires a compute instance, a private distribution and the generation of signed URLs or Cookies - but can restrict based on almost anything (licensing, user login status, user profile fields and much more) 

As a solutions architect you need to be comfortable with both - you WILL have an exam question on this :)
![](../images/2021-09-18-10-45-02.png)

###### ONLY works on COUNTRY CODE

![](../images/2021-09-18-11-06-06.png)

###### 3rd PArty Geolocation
![](../images/2021-09-18-11-09-31.png)

###### Field- level encryption
Field-Level encryption allows CloudFront to encrypt certain sensitive data at the edge using a public key, ensuring its protection through all levels of an application stack. Only the corresponding private key can decrypt the data, meaning you have complete control over who has access.

## Lambda@Edge
Lambda@Edge allows cloudfront to run lambda function at CloudFront edge locations to modify traffic between the viewer and edge location and edge locations and origins.

https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/lambda-examples.html#lambda-examples-redirecting-examples
![](../images/2021-09-18-11-58-12.png)
![](../images/2021-09-18-12-00-21.png)