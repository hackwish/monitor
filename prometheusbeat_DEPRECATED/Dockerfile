FROM infonova/prometheusbeat:latest

LABEL mantainer=hackwish

USER root

#Main config
COPY ./prometheusbeat.yml /prometheusbeat.yml

RUN chown prometheusbeat. /prometheusbeat /prometheusbeat.yml /data

RUN chmod go-w /prometheusbeat.yml

USER prometheusbeat

EXPOSE 8080