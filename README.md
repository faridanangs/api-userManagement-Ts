# User Api Spec

## Register User

Endpoint : POST /api/users

Request Body : 
```json
{
    "username": "Jondoy",
    "password": "rahasia",
    "name": "JondDoi Soi"
}
```

Response Body (success) :
```json
{
    "data":{
        "username": "Jondoy",
        "name":"JonDoi Soi",
    }
}
```

Response Body (failed) :
```json
{
    "errors": "username must not blank, ...",
}
```

## Login User

Endpoint : POST /api/users/login

Request Body : 
```json
{
    "username": "Jondoy",
    "password": "rahasia",
}
```

Response Body (success) :
```json
{
    "data":{
        "username": "Jondoy",
        "name":"JonDoi Soi",
        "token": "nBHBUVGYvYFC"
    }
}
```

Response Body (failed) :
```json
{
    "errors": "username not found",
}
```

## Get User

Endpoint : GET /api/users/current

Request Header :
- X-Api-Token: token

Response Body (success) :
```json
{
    "data":{
        "username": "Jondoy",
        "name":"JonDoi Soi",
    }
}
```

Response Body (failed) :
```json
{
    "errors": "Unauthorized, ...",
}
```

## Update User

Endpoint : PATCH /api/users/current

Request Header :
- X-Api-Token: token


Request Body : 
```json
{
    "password": "rahasia", // tidak wajib
    "name": "JondDoi Soi" // tidak wajib
}
```

Response Body (success) :
```json
{
    "data":{
        "username": "Jondoy",
        "name":"JonDoi Soi",
    }
}
```

Response Body (failed) :
```json
{
    "errors": "Unauthorized, ...",
}
```

## Logout User
Endpoint : DELETE /api/users/current

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
    "errors": "Unauthorized, ...",
}
```
