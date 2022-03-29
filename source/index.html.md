---
title: Algodojo API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  # - shell
  # - ruby
  - python : Python
  # - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/algodjo'>Documentation Powered by Algodjo</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Algodjo API
---

# Introduction

Welcome to the Algodjo API! You can use our API to access Algodjo API endpoints, which can connect on various brokers, algodjo, and execute you automatic trading.

We have language bindings in Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Algodjo](https://github.com/slatedocs/algodjo). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

<!-- ```ruby
require 'algodjo'

api = Algodjo::APIClient.authorize!('meowmeowmeow')
``` -->

```python
import algodjo

class IB(algodojo.ib):
    def __init__(self) -> None:
        super().__init__()

if __name__ == "__main__":
    setting = {
        'ip': 'YOUR_IP',
        'port': 'YOUR_IB_GATEWAY_PORT',
        'clientId': 'YOUR_IB_GATEWAY_CLINETID',
        'token':'YOUR_TOKEN'
    }
    ib = IB()
    result = ib.sign(setting)
    time.sleep(2)
```
<!-- 
```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: meowmeowmeow"
``` -->

<!-- ```javascript
const algodjo = require('algodjo');

let api = algodjo.authorize('meowmeowmeow');
``` -->

> Make sure to replace `YOUR_TOKEN` with your API Token key.

Algodjo uses API keys to allow access to the API. You can register a new Algodjo API Token key at our [developer portal](http://example.com/developers).

Algodjo expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: YOUR_TOKEN`

<aside class="notice">
You must replace <code>YOUR_TOKEN</code> with your personal API Token key.
</aside>

# Algodojo Interactive Brokers (IB)

## Sign in IB

Establishing an IB API connection

>To sign, use this code:

```python
import algodjo

class IB(algodojo.ib):
    def __init__(self) -> None:
        super().__init__()

if __name__ == "__main__":
    setting = {
        'ip': 'YOUR_IP',
        'port': 'YOUR_IB_GATEWAY_PORT',
        'clientId': 'YOUR_IB_GATEWAY_CLINETID',
        'token':'YOUR_TOKEN'
    }
    ib = IB()
    result = ib.sign(setting)
    time.sleep(2)
```
> Make sure to replace `YOUR_IP` with your local IP or 127.0.0.1.<br />
Make sure to replace `YOUR_IB_GATEWAY_PORT` with your IB Gateway or TWS port.<br />
Make sure to replace `YOUR_IB_GATEWAY_CLINETID` with your IB Gateway or TWS clientId.

### Sign Function
`ib.sign()`

### Setting Parameters

Parameter | Default | Description
--------- | ------- | -----------
ip        | 127.0.0.1| Set to your local ip or set 127.0.0.1.
port      |          | Set to your ib gateway or tws port or set 127.0.0.1.
clientId  |          | Set to your ib gateway or tws clientId or set 127.0.0.1.
token     |          | Set to your algodojo token.

## XXX in IB

>To XXX, use this code:

```python
import algodjo
```
> The above command returns dict structured like this:
```dict
```
### XXX Function

`ib.XXX()`

### Setting Parameters

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.
</aside>

<!-- ================================================== -->
# Example

## Get All Algodojo
<!-- 
```ruby
require 'algodjo'

api = Algodjo::APIClient.authorize!('meowmeowmeow')
api.algodjo.get
``` -->

```python
import algodjo

api = algodjo.authorize('meowmeowmeow')
api.algodjo.get()
```

<!-- ```shell
curl "http://example.com/api/algodjo" \
  -H "Authorization: meowmeowmeow"
``` -->
<!-- 
```javascript
const algodjo = require('algodjo');

let api = algodjo.authorize('meowmeowmeow');
let algodjo = api.algodjo.get();
``` -->

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all algodjo.

### HTTP Request

`GET http://example.com/api/algodjo`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include algodjo that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten
<!-- 
```ruby
require 'algodjo'

api = Algodjo::APIClient.authorize!('meowmeowmeow')
api.algodjo.get(2)
``` -->

```python
import algodjo

api = algodjo.authorize('meowmeowmeow')
api.algodjo.get(2)
```
<!-- 
```shell
curl "http://example.com/api/algodjo/2" \
  -H "Authorization: meowmeowmeow"
``` -->
<!-- 
```javascript
const algodjo = require('algodjo');

let api = algodjo.authorize('meowmeowmeow');
let max = api.algodjo.get(2);
``` -->

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/algodjo/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten
<!-- 
```ruby
require 'algodjo'

api = Algodjo::APIClient.authorize!('meowmeowmeow')
api.algodjo.delete(2)
``` -->

```python
import algodjo

api = algodjo.authorize('meowmeowmeow')
api.algodjo.delete(2)
```

<!-- ```shell
curl "http://example.com/api/algodjo/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
``` -->

```javascript
const algodjo = require('algodjo');

let api = algodjo.authorize('meowmeowmeow');
let max = api.algodjo.delete(2);
```

> The above command returns JSON structured like this:

<!-- ```json
{
  "id": 2,
  "deleted" : ":("
}
``` -->

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/algodjo/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

