FROM prom/prometheus:v2.5.0
# https://hub.docker.com/r/prom/prometheus/tags/

ENV WEAVE_TOKEN=none

COPY conf /etc/prometheus/

ENTRYPOINT [ "/etc/prometheus/docker-entrypoint.sh" ]
CMD        [ "--config.file=/etc/prometheus/prometheus.yml", \
             "--storage.tsdb.path=/prometheus" ]


# Build
# docker login gitlab.bcowtech.de:5050
# docker build -t gitlab.bcowtech.de:5050/bcow/ops/docker-hub:prometheus-gaas.v0.0.1 . --no-cache
# docker push gitlab.bcowtech.de:5050/bcow/ops/docker-hub:prometheus-gaas.v0.0.1
