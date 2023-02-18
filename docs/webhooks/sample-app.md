# Sample App to demonstrate working of Webhooks Connection for Wiliot

## Github Repo

https://github.com/vyshakhbabji/wiliot-developer-docs/tree/master/demos/wiliot-demo-webhooks-nodejs

## Overview

This sample app demonstrates how to use Wiliot webhooks to receive events from Wiliot Cloud Platform. 
The app is written in Node.js and uses the Express framework. It also uses the [ngrok](https://ngrok.com/) tool to generate a webhook URL.

## Prerequisites

- [Node.js](https://nodejs.org/en/download/) installed on your machine
- [ngrok](https://ngrok.com/download) installed on your machine
- A Wiliot account. If you don't have one, you can [sign up here](https://wiliot.com/).
- A Wiliot device. If you don't have one, you can [buy one here](https://wiliot.com/).

## Setup

1. Clone this repository to your local machine.

2. Change directory to demos/wiliot-demo-webhooks-nodejs

```bash
$ cd demos/wiliot-demo-webhooks-nodejs
```

3. Run the following command to install the dependencies:

```bash
$ npm install
```

4. Run the following command to start the app:

```bash
$ npm start
```

5. You should see the following output in the terminal:

```bash
vyshakhbabji@Vyshakhs-Mini wiliot-demo-webhooks % npm start 

> demos@1.0.0 start
> node index.js

Starting ngrok . Please wait ...
Webhook url is ready to use. Your webhook url is :  https://6285-2600-1700-dd90-14f0-fc10-ab-3e0a-9a1b.ngrok.io/webhook



Starting express server....
Your webhookURL is:  https://6285-2600-1700-dd90-14f0-fc10-ab-3e0a-9a1b.ngrok.io/webhook
Started Server.... 
App is listening at http://localhost:8080
```

6. Copy the webhook url from the output and use it in the [setting-up-webhook-connection](webhooks/Setting-up-webhook-connection.md) process.

7. Open the ngrok dashboard at http://localhost:4040/inspect/http to inspect the events sent to your webhook url.

8. When you test the webhooks on Wiliot's management portal, you should see the events in the ngrok dashboard and in the terminal where you started the app similar to the following:

```bash
Event received: 
 Event Name  temperature 
 Value 35.5 
 StartTime  1675828046616   
 EndTime 1675828046616 
 OwnerId 607737204301 
 CreatedOn 1675828046616 
 AssetId testAsset 
 CategoryID testCategory 
 Confidence 0.50 
 KeySet [ (key: temperature, value: 35.5) ]
```