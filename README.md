# Spring Cloud Service Connector for Amazon S3 Services

This project provides a [Spring Cloud](https://github.com/spring-cloud/spring-cloud-connectors) service connector for Amazon S3 services brokered by the Cloud Foundry [s3-cf-service-broker](https://github.com/cloudfoundry-community/s3-cf-service-broker).

## Example Usage

Add the library to your project:

```
<dependency>
	<groupId>com.dingotiles</groupId>
	<artifactId>spring-cloud-s3-service-connector</artifactId>
	<version>0.2.0</version>
</dependency>
```

Bind an S3 service to your Cloud Foundry application.

Use Spring Cloud to get an `S3ServiceInfo` instance.

```
CloudFactory cloudFactory = new CloudFactory();
Cloud cloud = cloudFactory.getCloud();

S3ServiceInfo serviceInfo = (S3ServiceInfo) cloud.getServiceInfo("my-s3-service");
...  serviceInfo.getAccessKeyId();
...  serviceInfo.getSecretAccessKey();
...  serviceInfo.getBucket();
```

