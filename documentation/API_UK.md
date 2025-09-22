# MaGuru MonoCheckout Rest Api

## WebAPI список:

````
url="/V1/mono/checkout/callback" method="POST"
url="/V1/mono/checkout/promocodes" method="GET"
url="/V1/mono/checkout/postdeliveryfee" method="POST"
url="/V1/mono/checkout/updateStatusOrderById/:incrementId" method="GET"
url="/V1/mono/checkout/getOrderRedirectUrlPay/:incrementId" method="GET"
````

### POST зворотний виклик від mono щодо статусу замовлення

``
POST: /V1/mono/checkout/callback
``

```
формат - /V1/mono/checkout/callback
```

###### Заголовки запитів
````
Authorization:  anonymous
Content-Type:   application/js
````

###### Повернути логічне значення (bool)

**********************

### GET запит від mono - перевірити промокод

``
GET: /V1/mono/checkout/promocodes
``

```
формат - /V1/mono/checkout/promocodes?basket_id={basket_id}&phone_number={phone_number}&promo_code={promo_code}
```

###### Заголовки запитів
````
Authorization:  Bearer
Content-Type:   application/js
````

###### Повернути application/json

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

### POST запит від mono - отримати ціни на доставку

``
POST: /V1/mono/checkout/postdeliveryfee
``

```
формат - /V1/mono/checkout/postdeliveryfee
```

###### Заголовки запитів
````
Authorization:  anonymous
Content-Type:   application/js
````

###### Тіло запиту raw (json)

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

###### Повернути application/json

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

### GET оновити статус замовлення з mono

``
GET: /V1/mono/checkout/updateStatusOrderById/:incrementId
``

```
формат - /V1/mono/checkout/updateStatusOrderById/123456
```

###### Заголовки запитів
````
Authorization:  Bearer
Content-Type:   application/js
````

###### Повернути логічне значення (bool)

**********************

### GET URL-адреса форми оформлення замовлення в Mono

``
GET: /V1/mono/checkout/getOrderRedirectUrlPay/:incrementId
``

```
формат - /V1/mono/checkout/getOrderRedirectUrlPay/123456
```

````
Заголовки запитів
Authorization:  Bearer customer token
Content-Type:   application/js
````

###### Повернути логічне значення (bool) АБО лінк на оплату

````
false OR https://checkout.mono.bank/order/f2729a74-6dr2-4586-b825-841a546fede2
````