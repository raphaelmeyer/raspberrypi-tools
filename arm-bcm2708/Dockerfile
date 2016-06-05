FROM raphaelmeyer/base:1.0.1

MAINTAINER Raphael Meyer <raphael.meyer@bbv.ch>

USER root

COPY raspberrypi-tools.zip /tmp/
RUN unzip -d /opt/
RUN rm -rf /tmp/raspberrypi-tools.zip

USER user

CMD ["/bin/bash"]

VOLUME ["/workspace"]
WORKDIR /workspace

