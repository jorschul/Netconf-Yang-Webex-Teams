# Netconf-Yang-Webex-Teams
Getting operational data on a remote IOS XE device using NETCONF Yang, and posting the output in Webex Teams.

## Getting started
You now have to sart ngrok on port 8080. 

```./ngrok http 8080```

Then, use `./webhook_tools/post_webhook.py` to POST the two webhooks.
* One for when the bot is mentioned,
* one for when the bot is added in a room.

Don't forget to edit the `./core/variables.py` file with your both token and the ngrok URL.

Then, execute the `./core/main.py` file.

## Tools
In order to facilite the creation and deletion of webhooks, two scripts can be executed. Both files are in `./webhooks_tools/`.
* `post_webhooks` will post two webhooks. One for when the bot is mentioned, one for when the bot is added to a room.
    * mentioned will be sent to `{url}/newmessage`
    * mentioned will be sent to `{url}/newroom`
* `delete_webhooks` will delete all active wehbooks.

