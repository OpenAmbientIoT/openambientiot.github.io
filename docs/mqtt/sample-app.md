# Sample App to demonstrate working of MQTT Connection for Wiliot

## Github Repo

https://github.com/vyshakhbabji/wiliot-developer-docs/tree/master/demos/wiliot-demo-mqtt-nodejs

## Overview

This sample app demonstrates how to use Wiliot MQTT connection to receive events from Wiliot Cloud Platform.

## Prerequisites

- [Node.js](https://nodejs.org/en/download/) installed on your machine
- A Wiliot account. If you don't have one, you can [sign up here](https://wiliot.com/).
- A Wiliot device. If you don't have one, you can [buy one here](https://wiliot.com/).
- HiveMQ MQTT configuration setup. Please follow the guide [hiveForMQTTUrl.md](hiveForMQTTUrl.md)

## Setup

1. Clone this repository to your local machine.

2. Change directory to demos/wiliot-demo-mqtt-nodejs

```bash
$ cd demos/wiliot-demo-mqtt-nodejs
```

3. Run the following command to install the dependencies:

```bash
$ npm install
```

4. Configure .env file with your HiveMQ MQTT configuration credentials. Please follow the guide [hiveForMQTTUrl.md](hiveForMQTTUrl.md)

```bash

4. Run the following command to start the app:

```bash
$ npm start
```

5. When you test the MQTT on Wiliot's management portal, you should see the events as output in the terminal:

```bash
vyshakhbabji@Vyshakhs-Mini wiliot-demo-mqtt-nodejs % npm start

> node-mqtt@1.0.0 start
> node index.js

Connected
Received message: 7B022D35-7373-489D-8503-C4266BFA7E32 {"eventName":"connectivity","value":"0","startTime":"1676000191728","endTime":"0","ownerId":"607737204301","createdOn":"1676000191986","assetId":"7B022D35-7373-489D-8503-C4266BFA7E32","categoryID":"12","confidence":"1.00","keySet":"[(key:connectivity,value:0)]"}
```
