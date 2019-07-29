FROM prom/prometheus

LABEL mantainer=hackwish

#Main config
COPY prometheus.yml /etc/prometheus/prometheus.yml

#Alerting rules
COPY ./alert-rules/record.rules.yml /alertmanager/record.rules.yml
COPY ./alert-rules/alert.rules.yml /alertmanager/alert.rules.yml

#Blackbox Jobs
COPY ./blackbox-jobs/ /blackbox/

#ENTRYPOINT ["bin/sh", "-c", "cat /hosts >> /etc/hosts && exec /bin/bash"]

#MOD ENTRYPOINT
# CMD cat /hosts >> /etc/hosts

ENTRYPOINT [ "/bin/prometheus", "--storage.tsdb.retention.time=7d", "--web.enable-admin-api", "--storage.tsdb.no-lockfile", "--storage.tsdb.min-block-duration=30m", "--storage.tsdb.max-block-duration=1d", "--config.file=/etc/prometheus/prometheus.yml", "--storage.tsdb.path=/prometheus" ]

EXPOSE 9090
