# spring-boot-ssl-truststore-gen [![Build Status](https://travis-ci.org/Orange-OpenSource/spring-boot-ssl-truststore-gen.svg?branch=master)](https://travis-ci.org/Orange-OpenSource/spring-boot-ssl-truststore-gen)


## Feature

Provides spring boot application with a [java SSL truststore](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html#CustomizingStores) made up of :
 * default truststore CA certificates
 * additional CA certificate extracted from a custom <i>TRUSTED_CA_CERTIFICATE_VALUE</i> System property

The [java SSL truststore](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jsse/JSSERefGuide.html#CustomizingStores) will be accessible through <i>javax.net.ssl.trustStore</i> and <i>javax.net.ssl.trustStorePassword</i> system properties.

## Details

spring-boot-ssl-truststore-gen will register a [spring boot event listener](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-spring-application.html#boot-features-application-events-and-listeners) that reacts whenever an [ApplicationStartedEvent](http://docs.spring.io/autorepo/docs/spring-boot/1.2.0.M2/api/org/springframework/boot/context/event/ApplicationStartedEvent.html) is sent (at the start of a run, but before any processing except the registration of listeners and initializers).

## Building

To build the source you will need to install JDK 1.8.

spring-boot-ssl-truststore-gen uses Maven

```
$ ./mvn install
```

## Usage

To enable automatic truststore generation, all you need is to add spring-boot-ssl-truststore-gen dependency to you spring boot application.

Example for maven

```
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
		
		<dependency>
		    <groupId>com.github.snowch</groupId>
		    <artifactId>spring-boot-ssl-truststore-gen</artifactId>
		    <version>master</version>
		</dependency>
```

