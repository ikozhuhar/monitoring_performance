# Мониторинг производительности


#### <a name='toc'>Содержание</a>
1. [???](#1)
2. [???](#2)
3. [???](#3)
4. [???](#4)
5. [???](#5)
6. [Дополнительные источники](#6)



1. [Система мониторинга Prometheus](https://help.reg.ru/support/servery-vps/oblachnyye-servery/ustanovka-programmnogo-obespecheniya/sistema-monitoringa-prometheus#1)
2. [Установка и настройка Prometheus](https://timeweb.cloud/tutorials/servers/ustanovka-i-nastrojka-prometheus)


```
sudo docker network create -d bridge monitoring
sudo docker run -d --name=prometheus --network=monitoring --ip 10.10.10.10 -p 9090:9090 bitnami/prometheus:latest
sudo docker run -d --name=node_exporter --network=monitoring --ip 10.10.10.11 -p 9100:9100 carlosedp/node_exporter
sudo docker run -d --name=grafana --network=monitoring--ip 10.10.10.12 -p 3000:3000 grafana/grafana-enterprise
```


## [[⬆]](#toc) <a name='6'>Дополнительные источники</a>

- [Мониторинг с помощью SYSSTAT](https://otus.ru/nest/post/284/)
- [Удобство наблюдения, atop](https://habr.com/ru/articles/140010/)
- [TOP`ай сюда](https://habr.com/ru/articles/114082/)
- [Команда vmstat](https://www.ibm.com/docs/ru/aix/7.2?topic=monitoring-vmstat-command)
- [Linux Out-of-Memory Killer (OOM)](https://geckich.blogspot.com/2013/12/linux-out-of-memory-killer-oom.html)
- [Про память: OOM Killer](https://catap.ru/blog/2009/05/03/about-memory-oom-killer/0)
- [Perf Examples](https://www.brendangregg.com/perf.html)
- [Мониторинг производительности (https://cdn.otus.ru/media/public/e5/14/6___%D0%9C%D0%BE%D0%BD%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%BD%D0%B3_%D0%BF%D1%80%D0%BE%D0%B8%D0%B7%D0%B2%D0%BE%D0%B4%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%D1%81%D1%82%D0%B8_6-364648-e514b7.pdf)
