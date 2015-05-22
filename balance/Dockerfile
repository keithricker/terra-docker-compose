FROM haproxy:1.5
RUN groupadd haproxy
RUN useradd -g haproxy haproxy
COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg