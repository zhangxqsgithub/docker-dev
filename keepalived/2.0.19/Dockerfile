FROM registry.cn-hangzhou.aliyuncs.com/open_zail/centos:7

MAINTAINER zail <zzzzail.mail@gmail.com>


ENV K=keepalived-2.0.19
ENV KEEPALIVED_HOME=/usr/local/keepalived

RUN yum -y update && \
    yum install -y wget gcc openssl openssl-devel && \
    yum clean all

RUN wget https://www.keepalived.org/software/${K}.tar.gz && \
    tar -zxvf ${K}.tar.gz && \
    cd ${K} && \
    ./configure --prefix=${KEEPALIVED_HOME} --sysconf=/etc && \
    make && \
    make install

RUN rm -rf /${K}.tar.gz && \
    rm -rf /${K}

WORKDIR ${KEEPALIVED_HOME}

CMD ["/sbin/keepalived"]
