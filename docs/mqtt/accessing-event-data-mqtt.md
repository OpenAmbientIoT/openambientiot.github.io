# Accessing Event data from Wiliot cloud using MQTT

MQTT provides a quick and easy way to access your Assets' event data from Wiliot cloud. You can register it as an application endpoint/
connection on our platform, Wiliot cloud will start publishing the events to the broker. Now by subscribing to the same topic your application can
access the asset related information from the cloud.


Referred from https://mntolia.com/10-free-public-private-mqtt-brokers-for-testing-prototyping/ article, please find below a list of free to use public
and private MQTT brokers

## Private MQTT Broker

In a private broker, only devices that you set can publish and subscribe to the topics on the broker. You should use this
for production & prototyping.


## Public MQTT Broker

In a public broker, any device can publish and subscribe to topics on the broker. There is no privacy. Public brokers should
never be used in production. If you simply want to learn or play around with MQTT then use this.


If you want to install your own broker on your computer or virtual machine see this:
Installing Mosquitto Broker ob Ubuntu/Windows/Debian
The information in the tables were last updated on April 7th 2020.


## Public MQTT Broker

| Name      | Broker Address     | TCP Port | TLS Port   | WebSocket Port | Message Retention | Persistent Session | Sign Up Requred |
|-----------|--------------------|----------|------------|----------------|-------------------|--------------------|-----------------|
| Eclipse   | mqtt.eclipse.org   | 1883     | N/A        | 80, 443        | YES               | YES                | NO              |
| Mosquitto | test.mosquitto.org | 1883     | 8883, 8884 | 80             | YES               | YES                | NO              |
| HiveMQ    | broker.hivemq.com  | 1883     | N/A        | 8000           | YES               | YES                | NO              |
| Flespi    | mqtt.flespi.io     | 1883     | 8883       | 80, 443        | YES               | YES                | YES             |
| Dioty     | mqtt.dioty.co      | 1883     | 8883       | 8080, 8880     | YES               | YES                | YES             |
| Fluux     | mqtt.fluux.io      | 1883     | 8883       | N/A            | N/A               | N/A                | NO              |
| EMQX      | broker.emqx.io     | 1883     | 8883       | 8083           | YES               | YES                | NO              |


## Private MQTT Broker

| Name      | TCP Port    | TLS Port    | WebSocket Port | Message Retention | Persistent Session | QoS Levels |  
|-----------|-------------|-------------|----------------|-------------------|--------------------|------------|
| Azure     | NO          | 8883        | 443            | NO                | Limited            | 0, 1       |  
| AWS       | NO          | 8883        | 443            | NO                | Limited            | 0, 1       |  
| CloudMQTT | Custom Port | Custom Port | Custom Port    | NOT SURE          | YES                | 0, 1, 2    | 


## Registering an application endpoint in management portal

- Ensure that you have “Admin” access for the account you manage on Wiliot management portal
- Go to https://platform.wiliot.com
- Click on the Connections option
- Click on the Add New  button
- Give the application a name

![mqtt1.png](..%2Fscreenshots%2Fmqtt1.png)

- Under Endpoint category choose MQTT as Type
- Click Next
- Choose one of the free to use URL from the tables above and enter it along with the TCP port number in the URL textbox ex: mqtt://test.mosquitto.org:1883

![mqtt2.png](..%2Fscreenshots%2Fmqtt2.png)