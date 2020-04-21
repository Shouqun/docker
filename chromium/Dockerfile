FROM ubuntu:18.04
MAINTAINER Shouqun Liu
RUN dpkg --add-architecture i386 \
    && apt-get update && apt-get install -y vim gcc libtool make curl wget git lsb-release python openssh-server net-tools \
    && export DEBIAN_FRONTEND=noninteractive && apt-get install -y tzdata && ln -fs /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && dpkg-reconfigure --frontend noninteractive tzdata \
    && curl https://raw.githubusercontent.com/Shouqun/docker/master/chromium/scripts/install-build-deps.sh > /tmp/install-build-deps.sh \
    && chmod u+x /tmp/install-build-deps.sh && bash /tmp/install-build-deps.sh --no-chromeos-fonts \
    && curl https://raw.githubusercontent.com/Shouqun/docker/master/chromium/scripts/install-build-deps-android.sh > /tmp/install-build-deps-android.sh \
    && chmod u+x /tmp/install-build-deps-android.sh && bash /tmp/install-build-deps-android.sh \
    && apt-get clean all \
    && cd ~/ && git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git \
    && echo "PATH=~/depot_tools:$PATH" >> ~/.bashrc
