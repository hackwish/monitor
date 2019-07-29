FROM prom/blackbox-exporter

LABEL mantainer=hackwish

#Main config
COPY blackbox.yml /etc/blackbox_exporter/config.yml

EXPOSE      9115

ENTRYPOINT  [ "/bin/blackbox_exporter", "--config.file=/etc/blackbox_exporter/config.yml" ]