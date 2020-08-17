# media-management

[Media Management]

* Home Assistant
* Node-Red
* ESPHome
* Frigate
* Unifi Video
* ser2sock
* vernemq
* zwave2mqtt


# home-assistant

![](https://i.imgur.com/OMwEZYO.png)

This also installs a postgresql deployment for holding the Home Assistant state and history information

* [home-assistant.yaml](home-assistant/home-assistant.yaml)
* [postgresql.yaml](home-assistant/postgresql.yaml)
To migrate the PostGRE SQL database, you must migrate them using `pg_dump` since the container does not have busybox or SSH

When you want to export from locahost
```
pg_dump -C -h remotehost -U remoteuser dbname | psql -h localhost -U localuser dbname
```

When you want to import from remote
```
 pg_dump -C -h localhost -U carpenam homeassistant | psql -h 10.10.1.60 -U carpenam homeassistant
 ```

# node-red

![](https://i.imgur.com/XxN4KJK.png)

Rules-engine for automations

* [node-red.yaml](node-red/node-red.yaml)


# frigate

![](https://i.imgur.com/hv7bh6m.png)

Installs [frigate](https://github.com/blakeblackshear/frigate/): Realtime object detection on RTSP cameras with the Google Coral

* [frigate.yaml](frigate/frigate.yaml)


# ser2sock

[ser2sock](https://github.com/nutechsoftware/ser2sock) is a serial to socket redirector.  This is used to bridge a home alarm panel to home-assistant for home automation.

* [ser2sock.yaml](ser2sock/ser2sock.yaml)

# verenmq

![](https://i.imgur.com/VQ5AZIV.png)

[verenmq](https://github.com/vernemq/vernemq) is a clustered MQTT broker

* [verenmq.yaml](verenmq/verenmq.yaml)

# zwave2mqtt

![](https://i.imgur.com/p0hlTFG.png)

[zwave2mqtt](https://github.com/OpenZWave/Zwave2Mqtt) for controlling zwave devices from a connected zwave controller and publishing over MQTT

* [zwave2mqtt.yaml](zwave2mqtt/zwave2mqtt.yaml)


* IP addresses for home-automation namespace

|     Service    	| IP Address   	| Notes 	|
|:--------------:	|--------------	|-------	|
| frigate        	| N/A          	|       	|
| home-assistant 	| 10.201.40.60 	|       	|
| node-red       	| N/A          	|       	|
| ser2sock       	| N/A          	|       	|
| vernemq        	| 10.201.40.10 	|       	|
| unifi-video    	| 10.201.40.20 	|       	|
| zwave2mqtt     	| 10.201.40.30 	|       	|
| zigbee2mqtt    	| 10.201.40.40 	|       	|
| esphome       	| 10.201.40.50 	|       	|
