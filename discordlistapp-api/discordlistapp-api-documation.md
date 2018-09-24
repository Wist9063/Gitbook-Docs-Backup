---
description: A simple way of communicating between Discord List App and node.js
---

# Discordlistapp-api Documation

## discordlistapp-api

[![NPM](https://nodei.co/npm/discordlistapp-api.png?compact=true)](https://nodei.co/npm/discordlistapp-api/) [![Build Status](https://travis-ci.org/Wist9063/discordlistapp-api.svg?branch=master)](https://travis-ci.org/Wist9063/discordlistapp-api) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/c2d9c2694efa420da7bdd90b017f644f)](https://www.codacy.com/app/Wist9063/discordlistapp-api?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Wist9063/discordlistapp-api&amp;utm_campaign=Badge_Grade) [![Greenkeeper badge](https://badges.greenkeeper.io/Wist9063/discordlistapp-api.svg)](https://greenkeeper.io/)

A simple way of communicating between Discord List App and node.js.

### Client

To start the client do the following:

```javascript
const discordlistapp = require('discorclistapp-api');
const discordlistclient = new discordlistapp.Client('YourTokenHere', 'YourBotIDHere');
```

#### 

{% api-method method="get" host="discordlistclient" path=".getBot\(id\)" %}
{% api-method-summary %}
getBot
{% endapi-method-summary %}

{% api-method-description %}
Used getting info on a certain bot.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
The ID of the bot.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "avatar": "9c382b6bc6c76a6d0b83baa5362051e0", 
  "discriminator": "0473", 
  "id": "341980888239702017", 
  "invite": "https://discordapp.com/oauth2/authorize?client_id=341980888239702017&scope=bot&permissions=3533830", 
  "library": "discord.js", 
  "long_description": "Jennifer, the new girl on the block. With lots of features listed below\r\nFeatures:\r\nModeration:\r\n- Kicking\r\n- Banning\r\n- Moderation Log\r\n- Message Pruning\r\nFun:\r\n- Dice Rolling\r\n- Coin Flipping\r\n- 8ball\r\n- Crime Coefficient\r\n- ASCII faces\r\n- Coin Flipping\r\n- Movie & TV lookup!\r\nUtility:\r\n- Server Information\r\n- User Information Fetching w/ User Avatar Displaying\r\n- Role Information\r\n- UserRole lookup\r\n- Member Count\r\n\r\nAnd more!", 
  "name": "Jennifer", 
  "owner_id": "166228540214214657", 
  "owner_name": "Wistful__#9063", 
  "prefix": "j) or J) | @Jennifer", 
  "short_description": "ennifer, the new girl on the block. With multiple Moderation, Utility, Lookup, & Fun commands. (ITS NOT JUST A GIRL :D)", 
  "support_server": "https://discord.gg/0xxkiR1rO4zRsYLp", 
  "username": "Jennifer#0473", 
  "votes": 0, 
  "website": "https://hexaplexsoftware.ga/"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="discordlistclient" path=".postGuildCount\(count\)" %}
{% api-method-summary %}
postGuildCount
{% endapi-method-summary %}

{% api-method-description %}
Post your Server Count to Discord List App
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="count" type="string" required=true %}
Guild Count.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Bot ID" type="string" required=true %}
From the Client Snowflake
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
From the Client Snowflake
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="discordlistclient" path=".getVotes\(\)" %}
{% api-method-summary %}
getVotes
{% endapi-method-summary %}

{% api-method-description %}
Retrieves the users that have voted for a bot.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Bot ID" type="string" required=false %}
From the Client Snowflake
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=false %}
From the Client Snowflake
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
Data: {[0]: 66166172835385344}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="discordlistclient" path=".getGuildCount\(id\)" %}
{% api-method-summary %}
getGuildCount
{% endapi-method-summary %}

{% api-method-description %}
Retrieves the Guild Count of a bot
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="ID" type="string" required=false %}
The ID of the bot
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{"server_count": 500}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="discordlistclient" path=".getAllBots\(\)" %}
{% api-method-summary %}
getAllBots
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
JSON Array
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



