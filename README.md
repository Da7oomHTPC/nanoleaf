### Nanoleaf

From Section 7 of the [Nanoleaf Open API Reference](http://forum.nanoleaf.me/docs/openapi). Requires setting up a developer account and signing in to their developer portal.

![[nanoleaf logo](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/nanoleaf-logo.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/nanoleaf-logo.png)

Click the Run in Postman button below to import this Postman Collection and Environment into your local instance of the [Postman app](https://www.getpostman.com/apps).

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/b6c8948a002d2dcd6364#?env%5BNanoleaf%5D=W3sia2V5IjoiaXBBZGRyZXNzIiwidmFsdWUiOiIxOTIuMTY4LngueDoxNjAyMSIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJ0ZXh0In0seyJrZXkiOiJhdXRoVG9rZW4iLCJ2YWx1ZSI6IkFkZC1hLXVzZXItdG8tZ2VuZXJhdGUtYXV0aC10b2tlbiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJ0ZXh0In1d)

### Generate an authorization token

1. On the Nanoleaf controller, hold the on-off button for 5-7 seconds until the LED starts flashing in a pattern.
2. From the Postman app or your own app, send a POST request to the authorization endpoint within 30 seconds of activating pairing, like this (substituting the IP address and port for your central controller):

`http://192.188.x.x:16021/api/v1/new`

> **Finding your IP:** The IP address of your Nanoleaf can be found using your router. Once you have the Nanoleaf connected to your WiFi, go to your router webpage and browse the devices connected to your network. Once you find your Nanoleaf, you can see the IP assigned to the device. 

> Remember if you're accessing the Nanoleaf at a local IP address, like when your router assigns a local IP address to the connected devices, both the Nanoleaf device and the client accessing the Nanoleaf (Postman) must be on the same local network. For example, both the Nanoleaf and laptop with Postman should be connected to the same WiFi network.

The result returned will be a 32-character authorization token that you will use in all of your subsequent calls.

### Quickstart

1. [Update the Postman environment](https://www.getpostman.com/docs/v6/postman/environments_and_globals/manage_environments#editing-an-active-environment) with your IP and port.
2. If you already have an authorization token, update the Postman environment with your token. Otherwise, you will need to use the [Add a user](https://documenter.getpostman.com/view/1559645/RW1gEcCH#edd41442-c94f-49dc-977b-8180be92e018) `POST` request to generate an authorization token.

In this Postman collection, I added a Quickstart folder to group a handful of requests to demonstrate a possible workflow (visible in the pre-request and test script sections). The remaining folders are replicated from the [Nanoleaf Open API Reference](http://forum.nanoleaf.me/docs/openapi). For more details and to see example responses, check out the [collection documentation](https://documenter.getpostman.com/view/1559645/RW1gEcCH).

![[nanoleaf documentation](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/nanoleaf-documentation.png)](https://s3.amazonaws.com/postman-static-getpostman-com/postman-docs/nanoleaf-documentation.png)
