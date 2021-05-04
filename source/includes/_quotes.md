# Create a quote after selecting a plan

```shell
curl -H 'Host: api.dev.iglooinsure.com' -H 'x-access-token: <app_token>' -H 'Content-Type: application/json' -H 'User-Agent: demo/48 CFNetwork/1220.1 Darwin/20.3.0' -H 'x-axinan-authorization: <user_token>' -H 'Accept: application/json' -H 'Accept-Language: en-us' -H 'x-app-id: telenor-b683' --data-binary '{"plan_id":31,"insured_person":{"nrc_or_passport":"c12312","customer_name":"nam Nguyen","phone_prefix_number":"95","email":"email@domain.com","phone_number":"987651"},"insured_object":{"uuid":"<igloo_device_id>","model":"iPhone13,3","brand":"Apple","imei_number":""},"product_key":"Telenor-AYA-Sompo-MSP-Nil-Excess"}' --compressed 'https://api.qa.iglooinsure.com/v1/psp/customer/quotes?random=8815&sign=<dynamic_signature>&timestamp=1620115317'
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
	"policy_display_id": "PSP20210500003"
}
```

This endpoint is for creating a quote on igloo server, as a preparation for Activation.

### HTTP Request

`POST /v1/psp/customer/quotes`

### HTTP Request Headers

Parameter | Type | Description
--------- | ------- | -----------
x-access-token | string | Client Authentication token
x-axinan-authorization | string | User Authentication token

### HTTP Body Parameters

Parameter | Type | Required | Description
--------- | ------- | ----------- | -----------
plan_id | number | true | The selected plan's id
insured_person | object | true | Customer's information (*)
insured_object | object | true | Device's information (**)
product_key | string | true | The selected plan's product-key

(*) insured_person is an object with structure:
```json
  { 
    "nrc_or_passport": string,
    "customer_name": string,
    "phone_prefix_number": string,
    "email": string,
    "phone_number": string
  }
```

(*) insured_object is an object with structure:
```json
  { 
    "uuid": string,
		"model": string,
		"brand": string,
		"imei_number": string
  }
```

<aside class="info">
Notice — `uuid` or `imei_number` is managed by iglooSDK, please retreive the id from `iglooSDK.deviceId()`
</aside>