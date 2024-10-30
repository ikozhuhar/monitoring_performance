# monitoring

1. [Система мониторинга Prometheus](https://help.reg.ru/support/servery-vps/oblachnyye-servery/ustanovka-programmnogo-obespecheniya/sistema-monitoringa-prometheus#1)
2. [Установка и настройка Prometheus](https://timeweb.cloud/tutorials/servers/ustanovka-i-nastrojka-prometheus)


```
sudo docker network create -d bridge monitoring
sudo docker run -d --name=prometheus --network=monitoring --ip 10.10.10.10 -p 9090:9090 bitnami/prometheus:latest
sudo docker run -d --name=node_exporter --network=monitoring --ip 10.10.10.11 -p 9100:9100 carlosedp/node_exporter
sudo docker run -d --name=grafana --network=monitoring--ip 10.10.10.12 -p 3000:3000 grafana/grafana-enterprise
```
