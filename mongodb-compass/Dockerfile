FROM centos:7.6.1810

MAINTAINER  service@vip56.cn

ADD ./mongodb-compass-1.20.0.x86_64.rpm /usr/local

RUN yum install -y gtk3 /usr/local/mongodb-compass-1.20.0.x86_64.rpm

EXPOSE 80

CMD ['/usr/bin/mongodb-compass']