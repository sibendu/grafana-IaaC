FROM debian:8

ENV BASE_URL   https://raw.githubusercontent.com/sibendu/iac-grafana/main
ENV DASHBOARD_NAME   README.md
ENV GRAFANA_CONFIG_FOLDER   /grafana-efs 

COPY run.sh . 

RUN apt-get update && apt-get install -y wget

ENTRYPOINT ./run.sh



