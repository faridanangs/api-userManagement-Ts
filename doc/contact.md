# Contact Api Spec

## Create Contact
Endpoint : POST /api/contacts

Request Header :
- X-Api-Token: token

Request Body : 
```json
{
    "first_name": "Jondoy",
    "last_name": "rahasia",
    "email": "JondDoi Soi",
    "phone": "081222222",
}
```

Response Body (success) :
```json
{
    "data":{
        "id": 1,
        "first_name": "Jondoy",
        "last_name": "rahasia",
        "email": "JondDoi Soi",
        "phone": "081222222",
    }
}
```

Response Body (failed) :
```json
{
    "errors": "first_name must not blank, ...",
}
```


## Get Contact
Endpoint : GET /api/contacts/:id

Request Header :
- X-Api-Token: token

Response Body (success) :
```json
{
    "data":{
        "id": 1,
        "first_name": "Jondoy",
        "last_name": "rahasia",
        "email": "JondDoi Soi",
        "phone": "081222222",
    }
}
```

Response Body (failed) :
```json
{
    "errors": "Contact is not found"
}
```


## Update Contact
Endpoint : PUT /api/contacts:id

Request Header :
- X-Api-Token: token

Request Body : 
```json
{
    "first_name": "Jondoy",
    "last_name": "rahasia",
    "email": "JondDoi Soi",
    "phone": "081222222",
}
```

Response Body (success) :
```json
{
    "data":{
        "id": 1,
        "first_name": "Jondoy",
        "last_name": "rahasia",
        "email": "JondDoi Soi",
        "phone": "081222222",
    }
}
```

Response Body (failed) :
```json
{
    "errors": "first_name must not blank, ...",
}
```

## Remove Contact
Endpoint : DELETE /api/contacts/:id

Request Header :
- X-Api-Token: token


Response Body (success) :
```json
{
    "data":"OK",
}
```

Response Body (failed) :
```json
{
    "errors": "Contact is not found"
}
```


## Search Contact
Endpoint : GET /api/contacts/

Request Header :
- X-Api-Token: token

Query Parameters:
- name : string, contact first_name or last_name, optional
- phone : string, contact number, optional
- email : string, contact email, optional
- page : number, default 1,
- size : number, default 10,


Response Body (success) :
```json
{
    "data":[
    {
        "id": 1,
        "first_name": "Jondoy",
        "last_name": "rahasia",
        "email": "JondDoi Soi",
        "phone": "081222222",
    },
    {
        "id": 1,
        "first_name": "Jondoy",
        "last_name": "rahasia",
        "email": "JondDoi Soi",
        "phone": "081222222",
    }
    ],
    "paging": {
        "current_page": 1,
        "total_page": 10,
        "size": 10
    }
}
```

Response Body (failed) :
```json
{
    "errors": "Unauthorized"
}
```
