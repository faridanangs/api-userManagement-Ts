# Address Api Spec

## Create Address
Endpoint : POST /api/contacts/:idContact/addresses

Request Header :
- X-Api-Token: token

Request Body : 
```json
{
    "street": "Jalan Apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal-code": "12345",

}
```

Response Body (success) :
```json
{
    "data":{
        "id": 1,
        "street": "Jalan Apa",
        "city": "Kota apa",
        "province": "Provinsi apa",
        "country": "Negara apa",
        "postal-code": "12345"
    }
}
```

Response Body (failed) :
```json
{
    "errors":"postal_code is required",
}
```



## Get Address
Endpoint : GET /api/contacts/:idContact/addresses/:idAddress

Request Header :
- X-Api-Token: token


Response Body (success) :
```json
{
    "data":{
        "id": 1,
        "street": "Jalan Apa",
        "city": "Kota apa",
        "province": "Provinsi apa",
        "country": "Negara apa",
        "postal-code": "12345"
    }
}
```

Response Body (failed) :
```json
{
    "errors":"address is not found",
}
```


## Update Address

Endpoint : PUT /api/contacts/:idContact/addresses/:idAddress

Request Header :
- X-Api-Token: token

Request Body : 
```json
{
    "street": "Jalan Apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal-code": "12345",

}
```

Response Body (success) :
```json
{
    "data":{
        "id": 1,
        "street": "Jalan Apa",
        "city": "Kota apa",
        "province": "Provinsi apa",
        "country": "Negara apa",
        "postal-code": "12345"
    }
}
```

Response Body (failed) :
```json
{
    "errors":"postal_code is required",
}
```



## Remove Address
Endpoint : DELETE /api/contacts/:idContact/addresses/:idAddress

Request Header :
- X-Api-Token: token

Response Body (success) :
```json
{
    "data":"OK"
}
```

Response Body (failed) :
```json
{
    "errors":"Address is not found",
}
```

## List Address
Endpoint : GET /api/contacts/:idContact/addresses

Request Header :
- X-Api-Token: token


Response Body (success) :
```json
{
    "data":[
    {
        "id": 1,
        "street": "Jalan Apa",
        "city": "Kota apa",
        "province": "Provinsi apa",
        "country": "Negara apa",
        "postal-code": "12345"
    },
    {
        "id": 2,
        "street": "Jalan Apa",
        "city": "Kota apa",
        "province": "Provinsi apa",
        "country": "Negara apa",
        "postal-code": "12345"
    },
    ]
}
```

Response Body (failed) :
```json
{
    "errors":"Contact is not found",
}
```

