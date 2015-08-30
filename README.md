# unblibraries/hubot-slack
Docker container : leverages phusion/baseimage to deploy our hubot for slack.

## Usage
```
docker run --rm \
    --name hubot-slack \
    -e HUBOT_GOOGLE_API_KEY= \
    -e HUBOT_SLACK_TOKEN= \
    -e HUBOT_GOOGLE_CSE_ID= \
    -e HUBOT_GOOGLE_CSE_KEY= \
    -e REDIS_URL=redis://192.168.2.202:6379/hubotslack \
    unblibraries/hubot-slack
```
## Runtime/Environment Variables
* `HUBOT_GOOGLE_API_KEY` - (Optional) A Google Maps JavaScript API v3 key. This can be obtained through the [google developers console](http://stackoverflow.com/questions/22294128/how-can-i-get-google-map-api-v3-key).
* `HUBOT_SLACK_TOKEN` - (Required) The token issued from the Slack bot user page](https://api.slack.com/bot-users).
* `REDIS_URL` - (Optional) A redis url in fhe form redis://*PASSWORD*@*HOST*:*PORT*/*KEYPREFIX*. Without this, any data saved to the brain will not persist between restarts or nodes.
* `HUBOT_GOOGLE_CSE_ID` - (Optional) A google [Custom Search Engine](https://cse.google.com/cse/all) to use in searches. Without this, the images returned from the 'animate me' command will not be animated.
* `HUBOT_GOOGLE_CSE_KEY` - (Optional) A 'server' API key for the CSE API, available through the [google developers console](https://console.developers.google.com/project/hubotlibsystems) . Without this, the images returned from the 'animate me' command will not be animated.

## License
- unblibraries/hubot-slack is licensed under the MIT License:
  - http://opensource.org/licenses/mit-license.html
- Attribution is not required, but much appreciated:
  - `Hubot for Slack Docker Container by UNB Libraries`

## Credit
- Original work for this container was based on that of [Nathaniel Hoag](http://nathanielhoag.com/blog/2014/12/07/a-dockerized-slack-integrated-hubot/).
