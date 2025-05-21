---
title: "RabbitMQ configuration on Quarkus"
slug: rabbitmq-configuration-quarkus
description: "How to configure RabbitMQ in a Quarkus project using SmallRye Reactive Messaging."
date: "2025-05-21"
tags:
- quarkus
- rabbitmq
- microservices
---

In this post, I'll show how to configure RabbitMQ in a Quarkus project using the SmallRye Reactive Messaging extension. This setup enables you to easily create producers and consumers for message-driven microservices using RabbitMQ as the broker.

## Quarkus RabbitMQ Dependency

To get started, add the following dependency to your **pom.xml**:

```xml
<dependency>
    <groupId>io.quarkus</groupId>
    <artifactId>quarkus-messaging-rabbitmq</artifactId>
</dependency>
```
This dependency provides integration with RabbitMQ via the SmallRye Reactive Messaging framework.

## Producer Configuration

To send messages to a RabbitMQ exchange, inject an **Emitter** into your Quarkus bean as follows:

```java
import jakarta.inject.Inject;
import org.eclipse.microprofile.reactive.messaging.Channel;
import org.eclipse.microprofile.reactive.messaging.Emitter;

@Channel("{your-queue}")
Emitter<String> requestEmitter;
```
Use **requestEmitter.send("message")** to publish messages.

Then, configure the producer in **application.properties**:

```
mp.messaging.outgoing.{your-queue}.connector=smallrye-rabbitmq
mp.messaging.outgoing.{your-queue}.exchange.name={your-queue}
mp.messaging.outgoing.{your-queue}.host=localhost
mp.messaging.outgoing.{your-queue}.port=5672
mp.messaging.outgoing.{your-queue}.username=guest
mp.messaging.outgoing.{your-queue}.password=guest
```
You can replace **{your-queue}** with the appropriate name for your use case.

## Processor

To consume messages from a queue, create a method annotated with **@Incoming**. You can optionally use **@Blocking** if the processing logic is blocking:

```java
import org.eclipse.microprofile.reactive.messaging.Incoming;
import io.smallrye.common.annotation.Blocking;

@Incoming("{your-queue-to-process}")
@Blocking
public void process(String request) { }
```
Then, configure the consumer in **application.properties**:
```
mp.messaging.incoming.{your-queue-to-process}.connector=smallrye-rabbitmq
mp.messaging.incoming.{your-queue-to-process}.host=localhost
mp.messaging.incoming.{your-queue-to-process}.port=5672
mp.messaging.incoming.{your-queue-to-process}.username=guest
mp.messaging.incoming.{your-queue-to-process}.password=guest
mp.messaging.incoming.{your-queue-to-process}.queue.name={your-queue}
mp.messaging.incoming.{your-queue-to-process}.exchange.name={your-queue}
```

Again, replace **{your-queue-to-process}** and **{your-queue}** with the appropriate names for your application.

## Full Example

You can check a full project [here](https://github.com/leandersonandre/quarkus-rabbitmq-voting-system).
