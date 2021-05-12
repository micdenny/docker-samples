# Supported tags and respective `Dockerfile` links

- [`3.6.9`](https://github.com/micdenny/docker-samples/blob/master/rabbitmq/windows/3.6.9/Dockerfile)
- [`3.6.12`](https://github.com/micdenny/docker-samples/blob/master/rabbitmq/windows/3.6.12/Dockerfile)
- [`3.8.16`, `latest`](https://github.com/micdenny/docker-samples/blob/master/rabbitmq/windows/3.8.16/Dockerfile)

# What is RabbitMQ?

RabbitMQ is open source message broker software (sometimes called message-oriented middleware) that implements the Advanced Message Queuing Protocol (AMQP). The RabbitMQ server is written in the Erlang programming language and is built on the Open Telecom Platform framework for clustering and failover. Client libraries to interface with the broker are available for all major programming languages.

> [wikipedia.org/wiki/RabbitMQ](https://en.wikipedia.org/wiki/RabbitMQ)

![img](https://raw.githubusercontent.com/docker-library/docs/81187b7b50f5af5bdb64d75882f4d9c782ad52c3/rabbitmq/logo.png)

# How to use this image

## Running the daemon

One of the important things to note about RabbitMQ is that it stores data based on what it calls the "Node Name", which defaults to the hostname. What this means for usage in Docker is that we should specify `-h`/`--hostname` explicitly for each daemon so that we don't get a random hostname and can keep track of our data:

```
docker run -d --hostname my-rabbit --name some-rabbit micdenny/rabbitmq-windows
```

### Management Plugin

The [management plugin](https://www.rabbitmq.com/management.html) is installed and enabled by default, which is available on the standard management port of 15672, with the default username and password of `guest` / `guest`.

You can then go to `http://hostname:15672` in a browser and use `user`/`password` to gain access to the management console.