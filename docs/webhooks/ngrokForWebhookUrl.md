# Using nrgok for generating webhook url

For testing purposes, you can use [ngrok](https://ngrok.com/) to generate a webhook url. 
This is a simple tool that allows you to expose a web server running on your local machine to the internet.


## What is ngrok?

ngrok is a tool that creates a secure tunnel from a public endpoint to a locally running web service.
It allows you to expose a web server running on your local machine to the internet and provides a public URL for accessing locally hosted web applications and services, 
making it easy to test and demonstrate webhooks.

## How to use ngrok for generating webhook url?

1. Download ngrok from [here](https://ngrok.com/download)
2. Unzip the downloaded file
3. Run the following command in the terminal to start ngrok:

```bash
$ {PATH_TO_DOWNLOADED_FILE} ./ngrok http 3000
```

4. Copy the generated url and use it as a webhook url in the  [setting-up-webhook-connection](webhooks/Setting-up-webhook-connection.md) process


Here is an example of the output you should see in the terminal:

![ngrok-terminal.png](..%2Fscreenshots%2Fngrok-terminal.png)


You can inspect the events sent to your webhook url by using the ngrok dashboard at http://localhost:{PORT}/inspect/http

![ngrok_-_Inspect.png](..%2Fscreenshots%2Fngrok_-_Inspect.png)
