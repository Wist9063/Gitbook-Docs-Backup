# Serverlist Documentation

## Start the API

First install the package by running:

```text
$ npm i botlist.space-api
```

Once you installed the npm package, you can now use the package in your code:

```javascript
const botlistspaceAPI = require('botlist.space-api');

// Now call the API code
const api = new botlistspaceAPI.serverlistAPI('InsertUserKeyHere');
```

{% hint style="danger" %}
Remember like the botlist counterpart, most of the functions require a user key.
{% endhint %}

## Functions with the API

Now that you have the your code set up, you can now use the API with a user key.

{% hint style="danger" %}
Please remember like I said, a user key is need for **MOST** functions with the api.

## ALL FUNCTIONS BELOW NEED A USER KEY.
{% endhint %}

For more info on the functions like response go [here](https://botlistspace.gitbook.io/api/sl-docs/general). 

{% api-method method="get" host="api." path="getServer\(id\)" %}
{% api-method-summary %}
Get Server
{% endapi-method-summary %}

{% api-method-description %}
Fetches info about a specific server by ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Server ID
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
    "id": "387812458661937152", // String
    "name": "botlist.space", // String
    "icon": "https://cdn.discordapp.com/icons/387812458661937152/e56ff74366e752e7817349235057504f.jpg?size=256", // String
    "short_description": "The official support server for botlist.space.", // String
    "full_description": "...", // ?String
    "icon_child_friendly": true, // Boolean
    "public": true, // Boolean
    "compliance": true, // Boolean
    "owners": [ // Array<Object>
        {
            "avatar": "https://cdn.discordapp.com/avatars/149505704569339904/d7083005cb77b45b55d82a4e1fbe104c.png?size=256", // String
            "discriminator": "0123", // String
            "id": "149505704569339904", // String
            "short_description": null, // ?String
            "username": "luke" // String
        }
    ],
    "tags": [ // ??Array<String>
        "Utility"
    ],
    "member_count": 2500, // Number
    "vanity": "botlist" // ?String
    "created_at": 1509302556022, // Number
    "updated_at": 1546153941801, // Number
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getALLServers\(pageNumb\)" %}
{% api-method-summary %}
Get All Servers
{% endapi-method-summary %}

{% api-method-description %}
Fetches ALL servers on the website per page.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="pageNumb" type="string" required=false %}
Page number. Will default to 1.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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
    "servers": [ // Array<Object>
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

{% api-method method="get" host="api." path="getStats\(\)" %}
{% api-method-summary %}
Get Stats
{% endapi-method-summary %}

{% api-method-description %}
Fetches info about the site.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": true, // Boolean
    "servers": 100, // Number
    "tags": 15, // Number
    "users": 2500 // Number
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getUser\(id\)" %}
{% api-method-summary %}
Get User
{% endapi-method-summary %}

{% api-method-description %}
Fetches user by ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
N/A
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getUserServers\(id, pageNumb\)" %}
{% api-method-summary %}
Get User Servers
{% endapi-method-summary %}

{% api-method-description %}
Fetches user's servers by ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
User ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="pageNumb" type="string" required=false %}
Page number
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
N/A
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="api." path="getUpvotes\(pageNumb, auth, id\)" %}
{% api-method-summary %}
Get Server Upvotes
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Server ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="auth" type="string" required=true %}
Your server's key.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="pageNumb" type="string" required=false %}
Page number. Will default to 1.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

