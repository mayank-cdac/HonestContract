# User

## Update Profile

This API is used for the update profile with the HonestContract application with some information.

```shell
curl -X PUT \
http://baseurl/api/user \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d '{
  "user":
    {
    "name": "Rajesh",
    "company_name": "Sony",
    "company_title": "Sony",
    "street": "44",
    "unit": "24",
    "street_name": "Sec 24",
    "city": "Gurgaon",
    "state": "Haryana",
    "country": "India",
    "pin": "110021",
    "email": "rajesh@gmail.com",
    "phone": "9898989898",
    "fax": "011-234446"
  }
}'
```


> The above command returns JSON structured like this:

```json
{
  "user":
    {
    "name": "Rajesh",
    "company_name": "Sony",
    "company_title": "Sony",
    "street": "44",
    "unit": "24",
    "street_name": "Sec 24",
    "city": "Gurgaon",
    "state": "Haryana",
    "country": "India",
    "pin": "110021",
    "email": "rajesh@gmail.com",
    "phone": "9898989898",
    "fax": "011-234446"
  }
}
```


### HTTP Request

`PUT http://baseurl/api/user`


Parameter | Type    | Description | Required
--------- | ------- | ----------- | -----------
name     | string | Name of the user | true
company_name| string | Company name          | true
company_title| string | Title of the company  | true
street    |string     | Street number of the company |false
unit      | string    | Unit of the company |false
street_name | string  | Street name of the company |false
city      |  string | City nameof the company | false
state     |  string | State name of the company  | false
country   | string  | Country name of the Company | true
pin       |  int    | Postal code of the company | false
email     | string  | Email address of the user | true
phone     |  string    | phone number of the user | false
fax       | string     | Fax number of the company |false


<aside class="success">Status code :200 OK </aside>
<aside class="warning">Error code : 422 Unprocessable Entity</aside>

## Users List

This API is used for the show a list of all users(excluding current logged in user) with the HonestContract application with some information.

```shell
curl -X GET \
http://baseurl/api/users \
-H 'accept: application/json' \
-H 'cache-control: no-cache' \
-H 'content-type: application/json' \
-d '{

}'
```


> The above command returns JSON structured like this:

```json
{
	"users": [
		{
			"id": 3,
			"email": "mayank1@gmail.com",
			"name": "Mayank pratap",
			"company_name": null,
			"company_title": null,
			"street": null,
			"unit": null,
			"street_name": null,
			"city": null,
			"state": null,
			"country": null,
			"pin": null,
			"phone": null,
			"fax": null,
			"created_at": "2017-09-27 12:27:56",
			"updated_at": "2017-09-27 12:27:56"
		},
		{
			"id": 4,
			"email": "mayank11@gmail.com",
			"name": "Mayank pratap",
			"company_name": null,
			"company_title": null,
			"street": null,
			"unit": null,
			"street_name": null,
			"city": null,
			"state": null,
			"country": null,
			"pin": null,
			"phone": null,
			"fax": null,
			"created_at": "2017-09-28 11:15:58",
			"updated_at": "2017-09-28 11:15:58"
		}
	]
}
```


### HTTP Request

`GET http://baseurl/api/users`


<aside class="success">Status code :200 OK </aside>
<aside class="warning">Error code : 422 Unprocessable Entity</aside>