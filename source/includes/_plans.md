# Get Product Plans

> Make sure to replace `<app_token>`, `<user_token>`, `<app_id>` with your keys.

```shell
 curl -H 'Host: api.dev.iglooinsure.com' 
 -H 'x-access-token: <app_token>' 
 -H 'Content-Type: application/json' 
 -H 'x-axinan-authorization: <user_token>' 
 -H 'Accept: application/json' 
 -H 'Accept-Language: en-us' 
 -H 'User-Agent: demo/48 CFNetwork/1220.1 Darwin/20.3.0' 
 -H 'x-app-id: <app_id>' 
 --compressed 'https://api.qa.iglooinsure.com/v1/psp/customer/plans?brand=Apple&model=iPhone13,3&random=6247&sign=<dynamic_signature>&timestamp=1620114169'	
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
  "supported": true,
	"plan_groups": [{
		"premium_type": "monthly",
		"total": 2,
		"plans": [{
			"coverages": [{
				"min_excess": "0",
				"name": "repairable"
			}, {
				"min_excess": "0",
				"name": "repairable"
			}],
			"currency": "MMK",
			"id": 27,
			"max_claim_amount": "50000",
			"name": "Plan 1",
			"policy_type": "TypePSP",
			"premium": "830",
			"premium_type": "monthly",
			"product_key": "Telenor-AYA-Sompo-MSP-Nil-Excess"
		}, {
			"coverages": [{
				"min_excess": "0",
				"name": "repairable"
			}, {
				"min_excess": "0",
				"name": "unrepairable"
			}],
			"currency": "MMK",
			"id": 29,
			"max_claim_amount": "80000",
			"name": "Plan 2",
			"policy_type": "TypePSP",
			"premium": "1330",
			"premium_type": "monthly",
			"product_key": "Telenor-AYA-Sompo-MSP-Nil-Excess"
		}]
	}, {
		"premium_type": "yearly",
		"total": 3
		"plans": [{
			"coverages": [{
				"min_excess": "0",
				"name": "repairable"
			}, {
				"min_excess": "0",
				"name": "unrepairable"
			}],
			"currency": "MMK",
			"id": 28,
			"max_claim_amount": "50000",
			"name": "Plan 1",
			"policy_type": "TypePSP",
			"premium": "9960",
			"premium_type": "yearly",
			"product_key": "Telenor-AYA-Sompo-MSP-Nil-Excess"
		}, {
			"coverages": [{
				"min_excess": "0",
				"name": "repairable"
			}, {
				"min_excess": "0",
				"name": "unrepairable"
			}],
			"currency": "MMK",
			"id": 30,
			"max_claim_amount": "80000",
			"name": "Plan 2",
			"policy_type": "TypePSP",
			"premium": "15960",
			"premium_type": "yearly",
			"product_key": "Telenor-AYA-Sompo-MSP-Nil-Excess"
		}, {
			"coverages": [{
				"min_excess": "0",
				"name": "repairable"
			}, {
				"min_excess": "0",
				"name": "unrepairable"
			}],
			"currency": "MMK",
			"id": 32,
			"max_claim_amount": "100000",
			"name": "Plan 3",
			"policy_type": "TypePSP",
			"premium": "20040",
			"premium_type": "yearly",
			"product_key": "Telenor-AYA-Sompo-MSP-Nil-Excess"
		}]
	}]
}
```

This endpoint retrieves all supported plans for the current device.

### HTTP Request

`GET /v1/psp/customer/plans`

### HTTP Request Headers

Parameter | Type | Description
--------- | ------- | -----------
x-access-token | string | Client Authentication token
x-axinan-authorization | string | User Authentication token

### URL Parameters

Parameter | Type | Description
--------- | ------- | -----------
brand | string | Phone's brand, like Apple, Samsung, Huawei
model | string | Phone's model, like Galaxy S20, iPhone 11 Pro

<aside class="info">
Notice — The plans are different for every device type, base on Brand and Model
</aside>
