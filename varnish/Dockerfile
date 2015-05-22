FROM jacksoncage/varnish
RUN apt-get update
RUN apt-get install -y wget vim curl
ENV VARNISH_BACKEND_IP web

ADD default.vcl /etc/varnish/default.vcl
