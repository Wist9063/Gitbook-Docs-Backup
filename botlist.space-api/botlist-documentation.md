# Botlist Documentation

## NPM Package:

{% embed url="https://www.npmjs.com/package/botlist.space-api" caption="NPM Package. \(duh\)" %}

For support, DM Wistful\_\_\#9063 on discord.

## Start the API.

First install the package by running:

```
$ npm i botlist.space-api
```

Once you installed the npm package, you can now use the package in your code:

```javascript
const botlistspaceAPI = require('botlist.space-api');

// Now call the API code
const api = new botlistspaceAPI.botlistAPI('InsertUserKeyHere');
```

{% hint style="warning" %}
Note, a user key is needed for **MOST** functions with the api.
{% endhint %}

## Functions with the API.

Now that you have your code set up, you can now interact the API.

{% hint style="danger" %}
Please remember like I said, a user key is need for **MOST** functions with the api.

## ALL FUNCTIONS BELOW NEED A USER USER KEY.
{% endhint %}

**For more info on the functions like response, go** [**here**](https://botlistspace.gitbook.io/api/)**.**

{% api-method method="get" host="api." path="getBot\(\'InsertIDHere\'\)" %}
{% api-method-summary %}
Get Bot
{% endapi-method-summary %}

{% api-method-description %}
This function is used to get info about a bot. _**A user key is needed for this function.**_
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID of the bot.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Click here for more info.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "page": 1, // Number
    "page_count": 20, // Number
    "bots": [ // Array<Object>
        { ... },
        { ... },
        { ... }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getUser\(\'InsertIDHere\'\)" %}
{% api-method-summary %}
Get User
{% endapi-method-summary %}

{% api-method-description %}
This function is used to get info about a user. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID of user
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Click Here for more info.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "id": "507329700402561045", // String
    "username": "PassTheMayo", // String
    "discriminator": "1281", // String
    "avatar": "https://cdn.discordapp.com/avatars/507329700402561045/188e722beb5a696d9cd320d1b9b1fd2e.png?size=256", // String
    "short_description": "..." // ?String
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getStats\(\)" %}
{% api-method-summary %}
Get Stats
{% endapi-method-summary %}

{% api-method-description %}
The function get the stats about the website.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Click Here for more info.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "total_bots": 400, // Number
    "approved_bots": 390, // Number
    "unapproved_bots": 10, // Number
    "tags": 34, // Number
    "users": 2500 // Number
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="api." path="postStats\(guild, auth, id\)" %}
{% api-method-summary %}
Post Stats
{% endapi-method-summary %}

{% api-method-description %}
This functions is used to post your guild count. **THIS REQUIRES YOUR BOT KEY, NOT TOKEN.**
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="id" type="string" required=true %}
ID of the bot.
{% endapi-method-parameter %}

{% api-method-parameter name="auth" type="string" required=true %}
Your bot's key from the page. **NOT BOT TOKEN.**
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="shard-array" type="array" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="guild" type="string" required=true %}
Number of guilds. Can be used with Array and string.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Click here for more info.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "code": 200, // Number
    "message": "Successfully updated server count" // String
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getUpvotes\(pageNumb, auth, id\)" %}
{% api-method-summary %}
Get Upvotes
{% endapi-method-summary %}

{% api-method-description %}
This function is used to get you upvotes per page. **THIS REQUIRES YOUR BOT KEY, NOT TOKEN.**
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Your bot's id.
{% endapi-method-parameter %}

{% api-method-parameter name="pageNumb" type="string" required=false %}
Page number, defaults to 1.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="auth" type="string" required=true %}
Your bot's key from your page. **NOT BOT TOKEN.**
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Click here for more info.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "page": 2, // Number
    "page_count": 6, // Number
    "upvotes": [ // ??Array<Object>
        {
            "user": {
                "id": "507329700402561045", // String
                "username": "PassTheMayo", // String
                "discriminator": "1281", // String
                "avatar": "...", // String
                "short_description": "..." // ?String
            },
            "timestamp": 1546208945017 // Number
        },
        ...
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getAllBots\(pageNumb\)" %}
{% api-method-summary %}
Get All Bots
{% endapi-method-summary %}

{% api-method-description %}
This function is used to get all bots on a per page basis. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pageNumb" type="string" required=true %}
Number of page.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "page": 1, // Number
    "page_count": 20, // Number
    "bots": [ // Array<Object>
        { ... },
        { ... },
        { ... }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



