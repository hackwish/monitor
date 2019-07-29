FROM grafana/grafana

LABEL mantainer=hackwish

#Main config
COPY ./datasources.yaml /etc/grafana/provisioning/datasources/datasource.yaml
#COPY ./dashboards.yaml /etc/grafana/provisioning/dashboards/dashboards.yaml


ENV GF_INSTALL_PLUGINS=grafana-clock-panel,grafana-simple-json-datasource,camptocamp-prometheus-alertmanager-datasource,grafana-piechart-panel,grafana-kubernetes-app,simpod-json-datasource,michaeldmoore-multistat-panel,xginn8-pagerduty-datasource,grafana-sensu-app,snuids-trafficlights-panel,smartmakers-trafficlight-panel,michaeldmoore-annunciator-panel,farski-blendstat-panel,yesoreyeram-boomtable-panel,briangann-gauge-panel,jdbranham-diagram-panel,larona-epict-panel,natel-plotly-panel,grafana-polystat-panel,corpglory-progresslist-panel,snuids-radar-panel,gretamosa-topology-panel

EXPOSE 3000