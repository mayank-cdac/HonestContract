# Contracts

##Create Contract
With this API he/she can create his/her contract through his/her company.

```shell
curl -X POST \
http://baseurl/api/contract/create \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d '{
	"contract": {
		"name": "Party Agreement 2017",
		"type": "buyer",
		"seller_id":3,
		"buyer_country":"India",
        "seller_country":"China",
	}
}'
```

> The above command returns JSON structured like this:

```json
{
	"contract": {
    		"name": "Party Agreement 2017",
    		"seller_id": 3,
    		"contractor_id": 2,
    		"contractee_id": 3,
    		"buyer_id": 2,
    		"updated_at": "2017-09-29 07:20:50",
    		"created_at": "2017-09-29 07:20:50",
    		"id": 17,
    		"setup": {
    			"id": 6,
    			"contract_id": 17,
    			"units_to_be_sold": null,
    			"description": null,
    			"status": null,
    			"created_at": "2017-09-29 07:20:50",
    			"updated_at": "2017-09-29 07:20:50",
    			"filled_values": []
    		},
    		"product_and_price": {
    			"id": 6,
    			"contract_id": 17,
    			"selling_units": null,
    			"price_per_unit": null,
    			"currency": null,
    			"discount_percent": null,
    			"tax_amount": null,
    			"shipping_cost": null,
    			"total_price": null,
    			"export_duties": null,
    			"import_duties": null,
    			"additional_terms": null,
    			"status": 0,
    			"created_at": "2017-09-29 07:20:50",
    			"updated_at": "2017-09-29 07:20:50",
    			"filled_values": []
    		},
    		"payment": {
    			"id": 6,
    			"contract_id": 17,
    			"payment_timing": null,
    			"payment_value": null,
    			"late_charge_percent": null,
    			"payment_method": null,
    			"payment_method_value": null,
    			"status": 0,
    			"created_at": "2017-09-29 07:20:50",
    			"updated_at": "2017-09-29 07:20:50",
    			"filled_values": []
    		},
    		"shipping": {
    			"id": 6,
    			"contract_id": 17,
    			"shipping_time": null,
    			"shipping_duration": null,
    			"shipping_destination": null,
    			"purpose_title": null,
    			"discount": 0,
    			"discount_value": null,
    			"buyer_tax": 0,
    			"buyer_tax_for": null,
    			"shipping_cost": 0,
    			"shipping_cost_value": null,
    			"shipping_insurance": null,
    			"frieght_forwarder": null,
    			"additional_shipping": null,
    			"status": 0,
    			"created_at": "2017-09-29 07:20:50",
    			"updated_at": "2017-09-29 07:20:50",
    			"filled_values": []
    		},
    		"final_contract": {
    			"id": 6,
    			"contract_id": 17,
    			"breach_event": null,
    			"liability": null,
    			"country": null,
    			"state": null,
    			"dispute_arise": null,
    			"dispute_value": null,
    			"additional_terms": null,
    			"status": 0,
    			"created_at": "2017-09-29 07:20:50",
    			"updated_at": "2017-09-29 07:20:50",
    			"filled_values": []
    		}
    	}
}
```

### HTTP Request

`POST http://baseurl/api/contract/create`


Parameter | Type    | Description | Required
--------- | ------- | ----------- |-----------
name | string | Name of the contract | true
type | string | (seller/buyer)       | true
buyer_id/seller_id | string | id of the other user | true
buyer_country | string | country of the contract | true
seller_country | string | Name of the contract | true



<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>


##Show Contract
With this API he/she can show his/her contract through his/her company.

```shell
curl -X GET \
http://baseurl/api/contract \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d '{
	"contract":{
    		"id":12
    	}
}'
```

> The above command returns JSON structured like this:

```json
{
	"contract": {
    		"id": 12,
    		"name": "Party Agreement 2017",
    		"contractor_id": 2,
    		"contractee_id": 3,
    		"seller_id": 3,
    		"buyer_id": 2,
    		"buyer_country": null,
    		"seller_country": null,
    		"status": null,
    		"created_at": "2017-09-28 08:04:33",
    		"updated_at": "2017-09-28 08:04:33",
    		"setup": {
    			"id": 1,
    			"contract_id": 12,
    			"units_to_be_sold": 12,
    			"description": "description",
    			"status": null,
    			"created_at": "2017-09-28 08:04:33",
    			"updated_at": "2017-09-28 09:55:48",
    			"filled_values": [
    				{
    					"id": 16,
    					"user_id": 2,
    					"form_id": 1,
    					"hash_values": {
    						"description": "description",
    						"updated_at": "2017-09-28 09:55:48"
    					},
    					"form_class": "App\\FormSetup",
    					"status": 0,
    					"created_at": "2017-09-28 09:55:48",
    					"updated_at": "2017-09-28 09:55:48"
    				}
    			]
    		},
    		"product_and_price": {
    			"id": 1,
    			"contract_id": 12,
    			"selling_units": null,
    			"price_per_unit": null,
    			"currency": null,
    			"discount_percent": null,
    			"tax_amount": null,
    			"shipping_cost": null,
    			"total_price": null,
    			"export_duties": null,
    			"import_duties": null,
    			"additional_terms": null,
    			"status": 0,
    			"created_at": "2017-09-28 08:04:33",
    			"updated_at": "2017-09-28 08:04:33",
    			"filled_values": []
    		},
    		"payment": {
    			"id": 1,
    			"contract_id": 12,
    			"payment_timing": "other",
    			"payment_value": "20.00",
    			"late_charge_percent": 10,
    			"payment_method": "credit_card",
    			"payment_method_value": "300",
    			"status": 0,
    			"created_at": "2017-09-28 08:04:33",
    			"updated_at": "2017-09-28 09:59:33",
    			"filled_values": [
    				{
    					"id": 17,
    					"user_id": 2,
    					"form_id": 1,
    					"hash_values": {
    						"payment_value": 20,
    						"updated_at": "2017-09-28 09:59:33"
    					},
    					"form_class": "App\\FormPayment",
    					"status": 0,
    					"created_at": "2017-09-28 09:56:32",
    					"updated_at": "2017-09-28 09:59:33"
    				}
    			]
    		},
    		"shipping": {
    			"id": 1,
    			"contract_id": 12,
    			"shipping_time": "seller_reciept",
    			"shipping_duration": null,
    			"shipping_destination": "ABCD",
    			"purpose_title": "ABCD",
    			"discount": 0,
    			"discount_value": null,
    			"buyer_tax": 0,
    			"buyer_tax_for": null,
    			"shipping_cost": 0,
    			"shipping_cost_value": null,
    			"shipping_insurance": "ANCD",
    			"frieght_forwarder": null,
    			"additional_shipping": null,
    			"status": 0,
    			"created_at": "2017-09-28 08:04:33",
    			"updated_at": "2017-09-28 10:10:10",
    			"filled_values": [
    				{
    					"id": 19,
    					"user_id": 2,
    					"form_id": 1,
    					"hash_values": {
    						"shipping_time": "seller_reciept",
    						"shipping_destination": "ABCD",
    						"purpose_title": "ABCD",
    						"shipping_insurance": "ANCD",
    						"updated_at": "2017-09-28 10:10:10"
    					},
    					"form_class": "App\\FormShipping",
    					"status": 0,
    					"created_at": "2017-09-28 10:10:10",
    					"updated_at": "2017-09-28 10:10:10"
    				}
    			]
    		},
    		"final_contract": {
    			"id": 1,
    			"contract_id": 12,
    			"breach_event": null,
    			"liability": null,
    			"country": "US",
    			"state": "ABCD",
    			"dispute_arise": "arbitration",
    			"dispute_value": null,
    			"additional_terms": null,
    			"status": 0,
    			"created_at": "2017-09-28 08:04:33",
    			"updated_at": "2017-09-28 10:03:20",
    			"filled_values": [
    				{
    					"id": 18,
    					"user_id": 2,
    					"form_id": 1,
    					"hash_values": {
    						"state": "ABCD",
    						"updated_at": "2017-09-28 10:03:20",
    						"country": "US",
    						"dispute_arise": "arbitration"
    					},
    					"form_class": "App\\FormFinal",
    					"status": 0,
    					"created_at": "2017-09-28 10:02:36",
    					"updated_at": "2017-09-28 10:03:20"
    				}
    			]
    		}
    	}
}
```

### HTTP Request

`GET http://baseurl/api/contract`


Parameter | Type    | Description | Required
--------- | ------- | ----------- |-----------
id | integer | id of the contract | true




<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

##Contract List

This API is used for the contracts list of the he/she (user).

```shell
curl -X GET \
http://baseurl/api/contracts \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d '{
}
 ```

> The above command returns JSON structured like this:

```json
{
	"contracts": [
		{
			"id": 12,
			"name": "Party Agreement 2017",
			"contractor_id": 2,
			"contractee_id": 3,
			"seller_id": 3,
			"buyer_id": 2,
			"buyer_country": null,
			"seller_country": null,
			"status": null,
			"created_at": "2017-09-28 08:04:33",
			"updated_at": "2017-09-28 08:04:33"
		},
		{
			"id": 13,
			"name": "Party Agreement 2017",
			"contractor_id": 2,
			"contractee_id": 3,
			"seller_id": 3,
			"buyer_id": 2,
			"buyer_country": null,
			"seller_country": null,
			"status": null,
			"created_at": "2017-09-28 08:35:32",
			"updated_at": "2017-09-28 08:35:32"
		},
		{
			"id": 14,
			"name": "Party Agreement 2017",
			"contractor_id": 2,
			"contractee_id": 3,
			"seller_id": 3,
			"buyer_id": 2,
			"buyer_country": null,
			"seller_country": null,
			"status": null,
			"created_at": "2017-09-28 09:09:42",
			"updated_at": "2017-09-28 09:09:42"
		},
		{
			"id": 15,
			"name": "Party Agreement 2017",
			"contractor_id": 2,
			"contractee_id": 3,
			"seller_id": 3,
			"buyer_id": 2,
			"buyer_country": null,
			"seller_country": null,
			"status": null,
			"created_at": "2017-09-28 09:09:47",
			"updated_at": "2017-09-28 09:09:47"
		},
		{
			"id": 16,
			"name": "Party Agreement 2017",
			"contractor_id": 2,
			"contractee_id": 3,
			"seller_id": 3,
			"buyer_id": 2,
			"buyer_country": null,
			"seller_country": null,
			"status": null,
			"created_at": "2017-09-28 09:57:02",
			"updated_at": "2017-09-28 09:57:02"
		}
	]
}

```

### HTTP Request

`GET http://baseurl/api/contracts`


Parameter | Type    | Description | Required
--------- | ------- | ----------- |-----------
          |         |             | 
          |         |             |


<aside class="success">status:200 OK </aside>


## Update Setup
This API is used for update the setup.

```shell
curl -X PUT \
http://baseurlapi/contract/setup \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d '{
    "setup":{
		"id":1,
		"units_to_be_sold": 12,
		"description": "description"
	}
}
 ```

> The above command returns JSON structured like this:

```json
{
	"setup": {
		"id": 1,
		"contract_id": 12,
		"units_to_be_sold": 12,
		"description": "description",
		"status": null,
		"created_at": "2017-09-28 08:04:33",
		"updated_at": "2017-09-28 09:55:48"
	}
}
```

### HTTP Request

`PUT http://baseurl/api/contract/setup`


Parameter | Type    | Description | Required
--------- | ------- | ----------- |-----------
units_to_be_sold| integers  | Units of the purpose | true
purpose_image| image | Multiple Image of the purpose| false
description  | text | Description of the purpose | true
detail_description     | pdf | Description of the purpose | false

<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

## Update Product & Price

This API is used for product and price of the contract.

```shell
curl -X PUT \
http://baseurl/api/contract/:id/product_price \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d ' {
     	"product_and_price":{
        		"id":1,
        		"selling_units":10,
        		"price_per_unit":200,
        		"currency":"dollor",
        		"total_price":200,
        		"export_duties":"buyer",
        		"import_duties":"buyer"
        	}
     }
 ```

> The above command returns JSON structured like this:

```json
    {
    	"product_and_price": {
        		"id": 1,
        		"contract_id": 12,
        		"selling_units": 10,
        		"price_per_unit": 200,
        		"currency": "dollor",
        		"discount_percent": null,
        		"tax_amount": null,
        		"shipping_cost": null,
        		"total_price": 200,
        		"export_duties": "buyer",
        		"import_duties": "buyer",
        		"additional_terms": null,
        		"status": 0,
        		"created_at": "2017-09-28 08:04:33",
        		"updated_at": "2017-09-29 05:19:16"
        	}
    }
```

### HTTP Request

`PUT http://baseurl/api/contract/product/price`


Parameter | Type    | Description | Required 
--------- | ------- | ----------- |--------
selling_units| integer | Units to be sold | true
price_per_unit |  integer | Price per unit  | true
discount_percentage | integer | Discount percentage | false
tax_amount |  integer | Buyer pay the tax to seller| false
shipping_cost | integer | Shipping amount pay by buyer| false
total_price | integer | Total price with price with tax & discount| true
export_duties | text | (any/buyer/seller)Export charge responsibility | true
import_duties | text | (any/buyer/seller)Import charge responsibility | true
additional_terms  |  pdf    | Term document of payment & price | false



<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>

## Update Payment

This API is used for payment of the contract.

```shell
curl -X PUT \
http://baseurl/api/contract/payment \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d ' {
 	"payment":{
    		"id":1,
    		"payment_timing": "other",
    		"payment_value": 20,
    		"late_charge_percent": 10,
    		"payment_method": "credit_card",
    		"payment_method_value": 300

    	}
 }
```

> The above command returns JSON structured like this:

```json
{
	"payment": {
    		"id": 1,
    		"contract_id": 12,
    		"payment_timing": "other",
    		"payment_value": 20,
    		"late_charge_percent": 10,
    		"payment_method": "credit_card",
    		"payment_method_value": 300,
    		"status": 0,
    		"created_at": "2017-09-28 08:04:33",
    		"updated_at": "2017-09-29 04:46:41"
    	}
}
 ```

### HTTP Request

`PUT http://baseurl/api/contract/payment`

Parameter | Type    | Description | Required 
--------- | ------- | ----------- |--------
payment_timing|string| (before_date / payment_by_buyer / remainder_by_buyer / consignment / other) Timing payment option |true
payment_value| decimal |  Timing other payment option | false
late_charge_percent| integer |  Timing other payment option |
payment_method| string|(wire_transfer / credit_card / alipay / paypal / escrow)Timing other payment option |true
payment_method_value| string |  Timing other payment option |false


<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>



## Update Shipping

This API is used for shipping of the contract.

```shell
curl -X PUT \
http://baseurl/api/contract/shipping \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d ' {
     	"shipping":{
        		"id":1,
        		"shipping_time":"seller_reciept",
        		"shipping_destination":"ABCD",
        		"purpose_title":"ABCD",
        		"shipping_insurance":"ANCD"
        	}
     }
```

> The above command returns JSON structured like this:

```json
{
	"shipping": {
    		"id": 1,
    		"contract_id": 12,
    		"shipping_time": "seller_reciept",
    		"shipping_duration": null,
    		"shipping_destination": "ABCD",
    		"purpose_title": "ABCD",
    		"discount": 0,
    		"discount_value": null,
    		"buyer_tax": 0,
    		"buyer_tax_for": null,
    		"shipping_cost": 0,
    		"shipping_cost_value": null,
    		"shipping_insurance": "ANCD",
    		"frieght_forwarder": null,
    		"additional_shipping": null,
    		"status": 0,
    		"created_at": "2017-09-28 08:04:33",
    		"updated_at": "2017-09-28 10:10:10"
    	}
}
 ```



### HTTP Request

`PUT http://baseurl/api/contract/shipping`


Parameter | Type    | Description | Required 
--------- | ------- | ----------- |--------
shipping_time|string|(before_date / seller_reciept / agreement_days / other) Shipping time option | true
shipping_duration|string| Shipping duration  | false
shipping_destination|string| Shipping destination  | true
purpose_title|string| Purpose title  | true
discount|string| Discount | false
discount_value|string| Discount value | false
buyer_tax|string| Buyer tax | false
buyer_tax_for|string| (sea / air / land) buyer tax for | false
shipping_cost|string| Shipping cost | false
shipping_cost_value|string| Shipping cost value | false
shipping_insurance|string| Shipping insurance | true
frieght_forwarder|string| Frieght forwarder | false
additional_shipping|string| Additional shipping | false


<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>



## Update Final Agreement

This API is used for the final agreement of the contract.

```shell
curl -X PUT \
http://baseurl/api/contract/final \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d ' {
 	"final_contract":{
    		"id":1,
    		"country":"US",
    		"state":"ABCD",
    		"dispute_arise":"arbitration"
    	}
 }
```

> The above command returns JSON structured like this:

```json
{
	"final_contract": {
    		"id": 1,
    		"contract_id": 12,
    		"breach_event": null,
    		"liability": null,
    		"country": "US",
    		"state": "ABCD",
    		"dispute_arise": "arbitration",
    		"dispute_value": null,
    		"additional_terms": null,
    		"status": 0,
    		"created_at": "2017-09-28 08:04:33",
    		"updated_at": "2017-09-28 10:03:20"
    	}
}
 ```

### HTTP Request

`PUT http://baseurl/api/contract/final`


Parameter | Type    | Description | Required 
--------- | ------- | ----------- |--------
breach_event| string | Event breach option |false
liability| string | (any / seller / buyer / no_event) Liability |false
country| string | Country |true
state| string | State |true
dispute_arise| string | (arbitration / litigation / prevailing)Dispute arise |true
dispute_value| string | Dispute arise value |false
additional_terms| string | Additional terms |false



<aside class="success">status:200 OK </aside>
<aside class="warning">status:422 Unprocessable entry.</aside>






























