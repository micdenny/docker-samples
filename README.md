# Instruction

## Build image

### RabbitMQ

```shell
docker build -t micdenny/rabbitmq-windows:3.6.9 ./rabbitmq/windows/3.6.9
docker build -t micdenny/rabbitmq-windows:3.6.12 ./rabbitmq/windows/3.6.12
docker build -t micdenny/rabbitmq-windows:3.8.16 ./rabbitmq/windows/3.8.16
docker build -t micdenny/rabbitmq-windows:3.9.8 ./rabbitmq/windows/3.9.

docker build -t micdenny/rabbitmq-windows:latest ./rabbitmq/windows/latest
```

#### Build for specific Windows Server versions 
```powershell
docker build -t micdenny/rabbitmq-windows:3.8.35-servercore-ltsc2019 ./rabbitmq/windows/3.8.35 --build-arg SERVER_VERSION=ltsc2019 
docker build -t micdenny/rabbitmq-windows:3.8.35-servercore-ltsc2012 ./rabbitmq/windows/3.9.35 --build-arg SERVER_VERSION=ltsc2022 
docker build -t micdenny/rabbitmq-windows:3.9.22-servercore-ltsc2019 ./rabbitmq/windows/3.9.22 --build-arg SERVER_VERSION=ltsc2019 
docker build -t micdenny/rabbitmq-windows:3.9.22-servercore-ltsc2012 ./rabbitmq/windows/3.9.22 --build-arg SERVER_VERSION=ltsc2022 
docker build -t micdenny/rabbitmq-windows:3.10.7-servercore-ltsc2019 ./rabbitmq/windows/3.10.7 --build-arg SERVER_VERSION=ltsc2019 
docker build -t micdenny/rabbitmq-windows:3.10.7-servercore-ltsc2012 ./rabbitmq/windows/3.10.7 --build-arg SERVER_VERSION=ltsc2022
```
### Redis

```shell
docker build -t micdenny/redis-windows:2.8 ./redis/windows/2.8
docker build -t micdenny/redis-windows:3.0 ./redis/windows/3.0
docker build -t micdenny/redis-windows:3.2 ./redis/windows/3.2
```
