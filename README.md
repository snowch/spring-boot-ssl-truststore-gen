## Feature

This library updates the certificates on java cloud foundry buildpacks with:

 * Default truststore CA certificates
 * Compose certificates provided in VCAP_SERVICES in the field ca_certificate_base64 

## Details

spring-boot-ssl-truststore-gen will register a [spring boot event listener](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-spring-application.html#boot-features-application-events-and-listeners) that reacts whenever an [ApplicationStartedEvent](http://docs.spring.io/autorepo/docs/spring-boot/1.2.0.M2/api/org/springframework/boot/context/event/ApplicationStartedEvent.html) is sent (at the start of a run, but before any processing except the registration of listeners and initializers).

## Building

To build the source you will need to install JDK 1.7+

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

