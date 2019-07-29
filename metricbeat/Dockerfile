FROM docker.elastic.co/beats/metricbeat:7.0.0

LABEL mantainer=hackwish

RUN ls -l

COPY metricbeat.yml /usr/share/metricbeat/metricbeat.yml

USER root

RUN chmod go-w /usr/share/metricbeat/metricbeat.yml 

USER metricbeat

RUN ./metricbeat modules enable prometheus


