# botkube

https://www.botkube.io/

![](https://i.imgur.com/yQ8sqtK.png)

* [botkube/botkube.yaml](botkube/botkube.yaml)

# influxdb

Metrics collection database

* [influxdb/influxdb.yaml](influxdb/influxdb.yaml)

# modem-stats

![](https://i.imgur.com/muHDysr.png)

Collect cable modem statistics for reporting

* [modem-stats/modem-stats.yaml](modem-stats/modem-stats.yaml)

# prometheus-operator

![](https://i.imgur.com/xFOepF3.png)

![](https://i.imgur.com/hTo49Uo.png)

Metrics and observability collection and dashboard software - also installs grafana

* [prometheus-operator/prometheus-operator.yaml](prometheus-operator/prometheus-operator.yaml)
* [prometheus-operator/prometheus-operator-helm-values.yaml](prometheus-operator/prometheus-operator-helm-values.yaml)

# speedtest

![](https://i.imgur.com/avohPk6.png)

ISP speed test results collector

* [speedtest/speedtest.yaml](speedtest/speedtest.yaml)

# uptimerobot

Based on this [custom helm chart](https://github.com/billimek/billimek-charts/tree/master/uptimerobot)

* [uptimerobot/uptimerobot.yaml](uptimerobot/uptimerobot.yaml)
* [uptimerobot/uptimerobot-helm-values.yaml](uptimerobot/uptimerobot-helm-values.yaml)



# LoadBalanceIP addresses for monitoring namespace
|       Service         	| IP Address       	| Notes 	|
|:------------------:    	|-----------------	|-------	|
| botkube                	| N/A             	|       	|
| influxdb               	| N/A             	| Didn't have a IP but has a LoadBalancer...not sure if it needs a static IP      	|
| modem-stats            	| N/A             	|       	|
| prometheus-operator    	| N/A             	|       	|
| speedtest-prometheus   	| N/A             	|       	|
| uptimerobot           	| N/A             	|       	|
| kubernetes-dashboard    |  N/A              |         |
