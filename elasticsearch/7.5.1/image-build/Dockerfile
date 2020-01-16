FROM registry.cn-hangzhou.aliyuncs.com/open_zail/elasticsearch:7.5.1

MAINTAINER zail <zzzzail.mail@gmail.com>


ADD ik /usr/share/elasticsearch/plugins/ik

USER root

RUN chown elasticsearch:elasticsearch /usr/share/elasticsearch/plugins/ik

USER elasticsearch
