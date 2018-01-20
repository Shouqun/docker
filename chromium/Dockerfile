FROM ubuntu:16.04
MAINTAINER Shouqun Liu
RUN apt-get update && apt-get install -y vim gcc libtool make curl wget git \
     && curl https://raw.githubusercontent.com/Shouqun/docker/master/chromium/scripts/install-build-deps-android.sh > /tmp/install-build-deps-android.sh \
	 && chmod u+x /tmp/install-build-deps-android.sh && bash /tmp/install-build-deps-android.sh \
	 && cd ~/ && git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git \
	 && echo "PATH=~/depot_tools:$PATH" >> ~/.bashrc

