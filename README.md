# MQTT over Websocket Monitor

Single page application MQTT over Websocket monitor.
Required libraries get from CDN, It works only the `.html` and Internet connection.

## Describe of `.html`

* `awsiot.html` : For AWS IoT. Support Pub/Sub using Amazon Cognito. (NOT using accessKey of IAM account)
    * In Amazon Cognito
        1. Create IdentityPool
        2. Get IdentityPoolId of *UnAuth*
    * In AWS IAM
        1. Attach *AWSIoTDataAccess* policy to Role of *UnAuth*
    * In Application
        1. Set IdentityPoolId to **CognitoIdentityPoolId for AWS IoT** and **Connect**
        2. Let's Pub/Sub!!
* `wss.html` : For MQTT over WebSocket.

## OneLiner WebServer

`.html` does not work in `file:///`. You need web server, but a little bit ime-consuming.

Try `$ python -m SimpleHTTPServer` if you have python2.7.

## License

MIT

EoT