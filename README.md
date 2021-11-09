# Instruction

## Build image

### RabbitMQ

```shell
docker build -t micdenny/rabbitmq-windows:3.6.9 ./rabbitmq/windows/3.6.9
docker build -t micdenny/rabbitmq-windows:3.6.12 ./rabbitmq/windows/3.6.12
docker build -t micdenny/rabbitmq-windows:3.8.16 ./rabbitmq/windows/3.8.16
docker build -t micdenny/rabbitmq-windows:3.9.8 ./rabbitmq/windows/3.9.8
docker build -t micdenny/rabbitmq-windows:latest ./rabbitmq/windows/latest
```

### Redis

```shell
docker build -t micdenny/redis-windows:2.8 ./redis/windows/2.8
docker build -t micdenny/redis-windows:3.0 ./redis/windows/3.0
docker build -t micdenny/redis-windows:3.2 ./redis/windows/3.2
```
