FROM elasticsearch:5-alpine

COPY ./config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo 'Asia/Shanghai' >/etc/timezone

# 数据存储文件不在版本库中
VOLUME [ "/usr/share/elasticsearch/data" ]
