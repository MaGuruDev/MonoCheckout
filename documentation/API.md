# MaGuru MonoCheckout Rest Api

## WebAPI list:

````
url="/V1/mono/checkout/callback" method="POST"
url="/V1/mono/checkout/promocodes" method="GET"
url="/V1/mono/checkout/postdeliveryfee" method="POST"
url="/V1/mono/checkout/updateStatusOrderById/:incrementId" method="GET"
url="/V1/mono/checkout/getOrderRedirectUrlPay/:incrementId" method="GET"
````

### POST callback from mono about status order

``
POST: /V1/mono/checkout/callback
``

```
format - /V1/mono/checkout/callback
```

###### Request Headers
````
Authorization:  anonymous
Content-Type:   application/js
````

###### Return bool

**********************

### GET request from mono - validate promo code

``
GET: /V1/mono/checkout/promocodes
``

```
format - /V1/mono/checkout/promocodes?basket_id={basket_id}&phone_number={phone_number}&promo_code={promo_code}
```

###### Request Headers
````
Authorization:  Bearer
Content-Type:   application/js
````

###### Return application/json

````
{
    "success": true,
    "code": 200,
    "data": {
        "total_amount": 19,
        "promo_codes": [
            {
                "promo_code": "testcoupon",
                "discount_amount": 1
            }
        ]
    }
}
````

**********************

### POST request from mono - get delivery prices

``
POST: /V1/mono/checkout/postdeliveryfee
``

```
format - /V1/mono/checkout/postdeliveryfee
```

###### Request Headers
````
Authorization:  anonymous
Content-Type:   application/js
````

###### Body raw (json)

````
{
    "orderRef": "1507322",
    "phoneNumber": "+380970014700",
    "methods": [
        "np_brnm",
        "np_box",
        "np_cargo",
        "courier"
    ],
    "city": "Дніпро",
    "address": "Відділення №78 (до 30 кг): Дніпро, Поля Олександра, 129р"
}
````

###### Return application/json

````
{
    "deliveryPriceList": [
        {
            "method": "np_box",
            "price": 25
        },
        {
            "method": "np_brnm",
            "price": 60
        },
        {
            "method": "np_cargo",
            "price": 110
        },
        {
            "method": "courier",
            "price": 70
        }
    ]
}
````

**********************

### GET update order status from mono

``
GET: /V1/mono/checkout/updateStatusOrderById/:incrementId
``

```
format - /V1/mono/checkout/updateStatusOrderById/123456
```

###### Request Headers
````
Authorization:  Bearer
Content-Type:   application/js
````

###### Return bool

**********************

### GET url to mono checkout form

``
GET: /V1/mono/checkout/getOrderRedirectUrlPay/:incrementId
``

```
format - /V1/mono/checkout/getOrderRedirectUrlPay/123456
```

````
Request Headers
Authorization:  Bearer customer token
Content-Type:   application/js
````

###### Return bool OR string

````
false OR https://checkout.mono.bank/order/f2729a74-6dr2-4586-b825-841a546fede2
````