FROM logstash:5-alpine

COPY ./conf.d /etc/conf.d

RUN mkdir -p /logs/output /logs/input

VOLUME [ "/logs/output", "/logs/input" ]

EXPOSE 5000
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo 'Asia/Shanghai' >/etc/timezone
ENTRYPOINT [ "logstash" , "-f" , "/etc/conf.d" ]
