FROM logstash:5.5.2

ADD ./logstash.conf /conf/logstash.conf

CMD [ "logstash", "-f","/conf/logstash.conf" ]