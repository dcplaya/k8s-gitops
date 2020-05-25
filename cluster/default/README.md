

# goldilocks

![](https://i.imgur.com/500FwQp.png)

Installs [goldilocks](https://github.com/FairwindsOps/goldilocks): to help with resource allocation selection

* [goldilocks.yaml](goldilocks/goldilocks.yaml)



# hubot

A bot for slack

* [hubot.yaml](hubot/hubot.yaml)

# minecraft

![](https://i.imgur.com/zBha0RP.png)

* [minecraft-creative.yaml](minecraft/minecraft-creative.yaml)
* [minecraft-survival.yaml](minecraft/minecraft-survival.yaml)

# minio

![](https://i.imgur.com/RF0aYAg.png)

S3-compatible bucket storage service

* [minio.yaml](minio/minio.yaml)



# nzbget

![](https://i.imgur.com/2KQbi2w.png)

Usenet download client

* [nzbget.yaml](nzbget/nzbget.yaml)

# plex

![](https://i.imgur.com/nDyS9OA.jpg)

* [plex.yaml](plex/plex.yaml)

# radarr

![](https://i.imgur.com/eAgWySC.png)

movie downloader

* [radarr.yaml](radarr/radarr.yaml)

# rtorrent-flood

![](https://i.imgur.com/ZtMrsbm.png)

torrent client

* [rtorrent-flood.yaml](rtorrent-flood/rtorrent-flood.yaml)



# sonarr

![](https://i.imgur.com/0CS5ADs.png)

tv show downloader

* [sonarr.yaml](sonarr/sonarr.yaml)

# tesla_dashcam

![](https://i.imgur.com/2tbqMGa.jpg)

[tesla_dashcam](https://github.com/ehendrix23/tesla_dashcam) is a kubernetes cron job that runs nightly to combine multiple different dashcam videos into a single multi-pane video from the car cameras.

* [tesla_dashcam.yaml](tesla_dashcam/tesla_dashcam.yaml)

# teslamate

![](https://i.imgur.com/qNlrxjH.png)
![](https://i.imgur.com/f12RcId.png)

[teslamate](https://github.com/adriankumpf/teslamate) is a tool and collection of grafana dashboards which collect metrics and observability data about your tesla vehicle.

* [teslamate.yaml](teslamate/teslamate.yaml)


* IP addresses for default namespace
 (Most of these are currently ignored by Flux, not going to give them IPs yet)

|     Service    	| IP Address   	| Notes 	|
|:--------------:	|--------------	|-------	|
| blocky        	| N/A          	| Needs moved to network-management namespace      	|
| goldilocks    	| N/A          	|       	|
| hubot         	| N/A          	|       	|
| minecraft      	| N/A          	|       	|
| minio         	| 10.201.40.10 	|       	|
| tesla_dashcam  	| N/A          	| Never use this 	|
| tesla_mate    	| N/A          	| Never use this 	|
