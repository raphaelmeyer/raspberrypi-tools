FROM raphaelmeyer/base:1.0.1

MAINTAINER Raphael Meyer <raphael.meyer@bbv.ch>

USER root

RUN apt-get update && apt-get install -y \
  cmake \
  git \
  make \
  unzip

COPY raspberrypi-tools.zip /tmp/
RUN unzip /tmp/raspberrypi-tools.zip tools-master/arm-bcm2708/gcc-linaro-arm-linux-gnueabihf-raspbian-x64/* -d /opt/
RUN rm -rf /tmp/raspberrypi-tools.zip

RUN mkdir -p /opt/cmake/
COPY raspbian.cmake /opt/cmake/

USER user

COPY entrypoint.sh /opt/
ENTRYPOINT ["/opt/entrypoint.sh"]
CMD ["/bin/bash"]

VOLUME ["/workspace"]
WORKDIR /workspace

