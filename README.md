
# eMQTT - Authz (Pro)

This application read a database (currently just MySQL) and take the information of the user and generate a credential to be use in MQTT Broker


## Pre Deploy

Make sure that the folder tree was created correctly, in case not change the folder of the logs in the file 'log4j2.xml' :

```xml
		<Property name="basePath">/eMQTT/eMQTT-Authz/logs/</Property>
```

Validate all the parameters included in the next export, it include database and mqtt connections parameters.

```Shell
	export EMQTT_DBNAME=datasynth
    export EMQTT_HOSTNAME=localhost
    export EMQTT_HOSTNAME_MQTT=localhost
    export EMQTT_PASSWORD=
    export EMQTT_PORT=3306
    export EMQTT_USERNAME=root
    export MQTT_PASSWORD=abcd1234
    export MQTT_USERNAME=Main

```


## Deployment

To deploy the application is requiered the user 'root' and then copy the files into the product folder:

```bash
  cp -R eMQTT-Authz/ /eMQTT
```

Assign permissions of execution to the launcher 'shell script':


```bash
  chmod +x Launcher-eMQTT-AuthZ.sh
```

Finally, to test the application is requiered to execute the following command (you can implement the service to deploy in higher environments):

```bash
  ./Launcher-eMQTT-AuthZ.sh &
```
