# Instruction

## Build image

### RabbitMQ

```shell
docker build -t micdenny/rabbitmq-windows:x.y.z ./rabbitmq/windows/x.y.z
docker build -t micdenny/rabbitmq-windows:x.y.z ./rabbitmq/windows/latest
```

#### Build for specific Windows Server versions 
```powershell
docker build -t micdenny/rabbitmq-windows:x.y.z-servercore-ltsc2019 ./rabbitmq/windows/x.y.z --build-arg SERVER_VERSION=ltsc2019 
docker build -t micdenny/rabbitmq-windows:x.y.z-servercore-ltsc2012 ./rabbitmq/windows/x.y.z --build-arg SERVER_VERSION=ltsc2022 
```
### Redis

```shell
docker build -t micdenny/redis-windows:x.y ./redis/windows/x.y
```
