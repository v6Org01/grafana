ARG REGISTRY
ARG REPO
ARG TAG
FROM ${REGISTRY}/${REPO}:${TAG}
LABEL maintainer="dev_lau11@a.jlv6.com"
LABEL os="alpine"
USER 0
RUN <<EOF
  mkdir /usr/share/grafana/public/custom-ui
  mkdir /usr/share/grafana/public/img/custom
EOF
COPY ./html/* /usr/share/grafana/public/custom-ui/
COPY ./img/* /usr/share/grafana/public/img/custom/
RUN <<EOP
  chown root:root /usr/share/grafana/public/custom-ui/
  chmod 755 /usr/share/grafana/public/custom-ui/
  chown root:root /usr/share/grafana/public/img/custom/
  chmod 755 /usr/share/grafana/public/img/custom/
EOP
USER 472
ENTRYPOINT ["/run.sh"]
