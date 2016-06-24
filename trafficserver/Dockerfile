FROM ubuntu:16.04
MAINTAINER Shouqun Liu
RUN apt-get update && apt-get install -y vim gcc libtool make libgnutls-dev tcl expat libpcre3 libpcre3-dev libcap-dev libhwloc-dev lua50 libncurses5-dev curl libssl-dev tcl-dev libexpat1-dev net-tools

RUN mkdir -p /trafficserver/build && \
     curl http://mirrors.tuna.tsinghua.edu.cn/apache/trafficserver/trafficserver-5.3.2.tar.bz2  > /trafficserver/build/trafficserver-5.3.2.tar.bz2 && \
     cd /trafficserver/build && tar -xjpf trafficserver-5.3.2.tar.bz2 && cd trafficserver-5.3.2 && \
     ./configure --prefix=/trafficserver  && make -j3 && make install

EXPOSE 8080
