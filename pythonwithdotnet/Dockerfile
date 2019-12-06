FROM python:3.6-slim

MAINTAINER  service@vip56.cn

USER root

COPY sources.list /etc/apt/sources.list

RUN apt-get update && apt-get install -y wget gnupg

RUN wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.asc.gpg && \
    mv microsoft.asc.gpg /etc/apt/trusted.gpg.d/ && \
    wget -q https://packages.microsoft.com/config/debian/9/prod.list && \
    mv prod.list /etc/apt/sources.list.d/microsoft-prod.list && \
    chown root:root /etc/apt/trusted.gpg.d/microsoft.asc.gpg && \
    chown root:root /etc/apt/sources.list.d/microsoft-prod.list

RUN apt-get install -y apt-transport-https && \
    apt-get update && \
    apt-get install -y dotnet-runtime-2.2

RUN rm -rf /var/lib/apt/lists/*
