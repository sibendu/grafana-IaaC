FROM ubuntu:latest

#RUN  apt-get install wget

COPY localhost.crt . 
COPY localhost.key .
COPY custom.ini .
COPY default.yaml .
COPY  grafana-7.3.4.linux-amd64.tar.gz  .
#.linux-amd64.tar.gz  grafana-7.3.4.linux-amd64.tar.gz 
#RUN wget https://dl.grafana.com/oss/release/grafana-7.3.4.linux-amd64.tar.gz

RUN tar -zxvf grafana-7.3.4.linux-amd64.tar.gz

RUN rm grafana-7.3.4.linux-amd64.tar.gz
#RUN cd grafana-7.3.4 && bin/grafana-server 

#RUN mv grafana-7.3.4/conf/defaults.ini  grafana-7.3.4/conf/defaults.ini.bkup

RUN cp custom.ini   grafana-7.3.4/conf/custom.ini

#RUN ls  grafana-7.3.4/conf/provisioning/
#RUN ls default.yaml

RUN cp default.yaml grafana-7.3.4/conf/provisioning/dashboards/default.yaml	
#RUN chmod 777 run.sh 

WORKDIR grafana-7.3.4

RUN ls -ltr bin

EXPOSE 443

CMD ["bin/grafana-server"]
#ENTRYPOINT [ "run.sh" ]











