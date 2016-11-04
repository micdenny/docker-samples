FROM microsoft/nanoserver

LABEL Description="Redis" Vendor="MSOpenTech" Version="3.2"

ENV maxmemory=500MB
ENV protected-mode=yes

EXPOSE 6379

WORKDIR /redis

RUN powershell -Command \
    $ErrorActionPreference = 'Stop'; \
    Invoke-WebRequest -Method Get -Uri https://github.com/MSOpenTech/redis/releases/download/win-3.2.100/Redis-x64-3.2.100.zip -OutFile redis.zip ; \
	Expand-Archive redis.zip . ; \
	Remove-Item redis.zip -Force

CMD redis-server --maxmemory %maxmemory% --protected-mode %protected-mode%
