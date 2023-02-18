# Using HiveMQ's MQTT broker for generating MQTT url

## What is HiveMQ?

HiveMQ is a commercial, high-performance MQTT broker software that enables the fast 
and reliable exchange of data between devices and applications that use MQTT as the communication protocol. 
It is designed to handle large numbers of connected devices and high message throughput.

HiveMQ offers features such as scalability, reliability, security, and easy integration with other systems, 
making it a popular choice for IoT solutions, M2M communication, and industrial automation. 
Additionally, HiveMQ provides a comprehensive set of management tools, monitoring capabilities, 
and a plugin architecture that allows for customization and extension of the platform.

## How to use HiveMQ's MQTT broker for generating MQTT url?

1. Go to [HiveMQ's MQTT broker](https://www.hivemq.com/mqtt-cloud-broker/) and click on the **Try out for Free** button.

2. Sign up for a free account and log in.

3. The console will ask you to 'Set up credentials for your IOT devices'. Enter a username and password and click on the **Add** button.
![Getting_Started_-_HiveMQ_Cloud.png](..%2Fscreenshots%2FGetting_Started_-_HiveMQ_Cloud.png)

4. Click on the **Overview** menu. 

5. You will see **Cluster URL** and **Port** information. Copy the **Cluster URL** and use it as a MQTT url in the [setting-up-mqtt-connection](setting-up-mqtt-connection.md) process.

Your MQTT url will look like this: `mqtts://<CLUSTER_URL>:<PORT>`

In this case, for example: `mqtt://4be23fb544cb4b26ac93ec4c2d5d78ab.s2.eu.hivemq.cloud:8883`

![Cluster_Details_-_HiveMQ_Cloud.png](..%2Fscreenshots%2FCluster_Details_-_HiveMQ_Cloud.png)

6. Continue with [setting-up-mqtt-connection](setting-up-mqtt-connection.md) process.