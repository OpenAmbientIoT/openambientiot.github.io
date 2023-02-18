# Setting up new Webhook Connection 

Setting up new Webhook Connection is a simple process.
First you need to create a Webhook URL and then you need to register this URL with Wiliot via Wiliot's Management Platform.

## Step 1: Login to Wiliot Management Platform

Login to https://platform.wiliot.com/ using your Wiliot credentials.  If you don't have a Wiliot account, 
you can create one by clicking on the "Create One" button.

![Login-Wiliot.png](..%2Fscreenshots%2FLogin-Wiliot.png)


## Step 2: Click on Connections and Add new button

Once you are logged in, click on Connections and then click on Add new button. 
This will open a new window where you can choose the type of connection you want to create.

![Wiliot-connections.png](..%2Fscreenshots%2FWiliot-connections.png)


## Step 3: Select Connection Type
For setting up Webhooks, we will select HTTP as connection type . Add a name for your connection and click Next.

![Wiliot_-_Webhook-Connection-2.png](..%2Fscreenshots%2FWiliot_-_Webhook-Connection-2.png)

Under 'Settings' tab, you can add your Webhook URL. Choose 'POST' as  HTTP Method and 
and select the events you want to receive.  Click on 'Save' button to save your settings. You can also edit these settings later. 

![Wiliot_Platform-body.png](..%2Fscreenshots%2FWiliot_Platform-body.png)

## Step 4: Test Webhook Setup

We provide a simple way to test your Webhook setup.  Under newly created connection, click on  3 to the right of the connection and select 'Test' option.  
This will send a test event to your Webhook URL.  You can check the event headers and body to verify that the event was sent successfully.

![Wiliot_Test.png](..%2Fscreenshots%2FWiliot_Test.png)

Here is an example of a test event sent to a Webhook URL:

```shell
POST /webhook HTTP/1.1
Host: db0c-2600-1700-dd90-14f0-fc10-ab-3e0a-9a1b.ngrok.io
User-Agent: okhttp/4.10.0
Content-Length: 247
Accept-Encoding: gzip, deflate
Content-Type: text/plain; charset=utf-8
X-Forwarded-For: 52.6.71.162
X-Forwarded-Proto: https

Event Name  temperature 
Value 35.5 
StartTime  1675824020128   
EndTime 1675824020128 
OwnerId 607737204301 
CreatedOn 1675824020128 
AssetId testAsset 
CategoryID testCategory 
Confidence 0.50 
KeySet [ (key: temperature, value: 35.5) ]
```








