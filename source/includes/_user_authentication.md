# User Authentication

> To authorize user, use this code:

```shell
curl -H 'Host: api.qa.iglooinsure.com' \
-H 'x-access-token: c2c013bdc8b...08534b1e02' \
-H 'Content-Type: application/json' \
-H 'User-Agent: demo/48 CFNetwork/1220.1 Darwin/20.3.0' \
-H 'Accept: application/json' \
-H 'Accept-Language: en-us' \
-H 'x-app-id: <APP_ID>' \
--data-binary '{"user_id":"namsg_001"}' \
--compressed 'https://api.qa.iglooinsure.com/v1/psp/auth?random=1448&sign=<dynamic_signature>&timestamp=1620114166'
```

```ruby

```

```python

```

```javascript

```

> The above command returns JSON structured like this:

```json
{
	"jwt_token": "eyJhbGciOiJIUzUxMiIsInR5cC...ifLn5g"
}
```

> This token will be added to the request headers for future request. [x-axinan-authorization: eyJhbGciOiJIUzUxMiIsInR5cC...ifLn5g]

igloo expects for the API key to be included in all API requests to the server in a header that looks like the following:

`x-axinan-authorization: eyJhbGciOiJIUzUxMiIsInR5cC...ifLn5g`

<aside class="notice">
You must replace <code>APP_ID</code> with your personal API keys.
</aside>