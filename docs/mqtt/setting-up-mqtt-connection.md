# Setting up new MQTT Connection

Setting up new Webhook Connection is a simple process.
First you need to create a [MQTT URL](hiveForMQTTUrl.md) and then you need to register this URL with Wiliot via Wiliot's Management Platform.

## Step 1: Login to Wiliot Management Platform

Login to https://platform.wiliot.com/ using your Wiliot credentials.  If you don't have a Wiliot account,
you can create one by clicking on the "Create One" button.

![Login-Wiliot.png](..%2Fscreenshots%2FLogin-Wiliot.png)


## Step 2: Click on Connections and Add new button

Once you are logged in, click on Connections and then click on Add new button.
This will open a new window where you can choose the type of connection you want to create.

![Wiliot-connections.png](..%2Fscreenshots%2FWiliot-connections.png)

## Step 3: Select Connection Type

For setting up MQTT, we will select MQTT as connection type . Add a name for your connection and click Next.

![Wiliot_MQTT-1.png](..%2Fscreenshots%2FWiliot_MQTT-1.png)

## Step 4: Add MQTT URL

Under 'Settings' tab, you can add your MQTT URL. Choose 'MQTT' as  Protocol and  paste your MQTT URL  in the URL field.
Choose topics you want to subscribe to  and  select the events you want to receive.  
Add the username and password for your MQTT URL. These credentials should be the one you used to `Set up credentials for your IOT devices` on HiveMQ 

![Wiliot_Platform-mqtt-connections.png](..%2Fscreenshots%2FWiliot_Platform-mqtt-connections.png)

## Step 5: Save the settings
Click on 'Add' button to save your settings. You can also edit these settings later.

## Step 6: Test MQTT Setup

We provide a simple way to test your MQTT setup.  Under newly created connection, click on  3 dots to the right of the connection and select 'Test' option.
This will send a test event to your MQTT URL.  You can check the event headers and body to verify that the event was sent successfully.

![Wiliot_Test.png](..%2Fscreenshots%2FWiliot_Test.png)

Here is an example of a test event sent to a MQTT URL:

```shell
Received message: coffee_cup_1669671577 {"eventName":"temperature","value":"22.0","startTime":"1676000167097","endTime":"0","ownerId":"607737204301","createdOn":"1676000215587","assetId":"coffee_cup_1669671577","categoryID":"coffeecup","confidence":"1.00","keySet":"[(key:temperature,value:22.0)]"}
```

