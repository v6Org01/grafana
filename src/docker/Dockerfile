ARG REGISTRY
ARG REPO
ARG TAG
FROM ${REGISTRY}/${REPO}:${TAG}
LABEL maintainer="dev_lau11@a.jlv6.com"
LABEL os="alpine"
USER 0
RUN mkdir /usr/share/grafana/public/img/custom
COPY ./img/* /usr/share/grafana/public/img/custom/
RUN chown root:root /usr/share/grafana/public/img/custom/
RUN chmod 755 /usr/share/grafana/public/img/custom/
USER 472
ENTRYPOINT ["/run.sh"]
