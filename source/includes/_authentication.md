# Authentication

> To authorize, use this code:

```shell
curl -H 'Host: api.dev.iglooinsure.com' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
--data-binary '{"app_key":<APP_KEY>,"app_secret":<APP_SECRET>,"app_id":<APP_ID>}' \
--compressed 'https://api.dev.iglooinsure.com/v1/app-auth/apps/api-keys'
```

```ruby

```

```python

```

```javascript

```

> Make sure to replace APP_KEY, APP_SECRET, APP_ID with yours. You can register a new iglooSDK API key at our [developer portal](http://developers.iglooinsure.com/). Or via email: nam.nguyen@iglooinsure.com

> The above command returns JSON structured like this:

```json
{
	"access_token": "c2c013bdc8b...08534b1e02"
}
```

> This token will be added to the request headers for future request. [x-access-token: c2c013bdc8b...08534b1e02]

igloo expects for the API key to be included in all API requests to the server in a header that looks like the following:

`x-access-token: c2c013bdc8b...08534b1e02`

<aside class="notice">
You must replace <code>APP_KEY</code>, <code>APP_SECRET</code>, <code>APP_ID</code> with your personal API keys.
</aside>