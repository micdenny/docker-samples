FROM microsoft/nanoserver

LABEL Description="Redis" Vendor="MSOpenTech" Version="3.0"

ENV maxmemory=500MB

EXPOSE 6379

WORKDIR /redis

RUN powershell -Command \
    $ErrorActionPreference = 'Stop'; \
    Invoke-WebRequest -Method Get -Uri https://github.com/MSOpenTech/redis/releases/download/win-3.0.504/Redis-x64-3.0.504.zip -OutFile redis.zip ; \
	Expand-Archive redis.zip . ; \
	Remove-Item redis.zip -Force

CMD redis-server --maxmemory %maxmemory%