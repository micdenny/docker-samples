FROM microsoft/nanoserver

LABEL Description="Redis" Vendor="MSOpenTech" Version="2.8"

ENV maxmemory=500MB

EXPOSE 6379

WORKDIR /redis

RUN powershell -Command \
    $ErrorActionPreference = 'Stop'; \
    Invoke-WebRequest -Method Get -Uri https://github.com/MSOpenTech/redis/releases/download/win-2.8.2402/Redis-x64-2.8.2402.zip -OutFile redis.zip ; \
	Expand-Archive redis.zip . ; \
	Remove-Item redis.zip -Force

CMD redis-server --maxmemory %maxmemory%