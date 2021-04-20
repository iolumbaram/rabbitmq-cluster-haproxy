FROM haproxy:1.7

ENV HAPROXY_USER haproxy

RUN groupadd -f --system ${HAPROXY_USER} \
    && id -u ${HAPROXY_USER} &>/dev/null || useradd ${HAPROXY_USER} \
    && mkdir -p /var/lib/${HAPROXY_USER} \
    && chown -R ${HAPROXY_USER}:${HAPROXY_USER} /var/lib/${HAPROXY_USER}

COPY ./haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg
COPY ./certs/ /etc/haproxy/certs/

CMD ["haproxy", "-f", "/usr/local/etc/haproxy/haproxy.cfg"]