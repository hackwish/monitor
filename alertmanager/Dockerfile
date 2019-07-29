FROM prom/alertmanager

LABEL mantainer=hackwish

#Main config
COPY ./notifications.tmpl /etc/alertmanager/notifications.tmpl
COPY ./alertmanager.yaml /etc/alertmanager/alertmanager.yml
