# Contact API Specs

## Create Contact API 
Endpoint : POST /api/contacts

Headers : 
- Authorization : token

Request Body : 
```json 
{
    "first_name": "Fathur",
    "last_name": "Walkers",
    "email": "fathurwalkers@gmail.com",
    "phone": "085342072402"
}
```

Request Body Success : 
```json 
{
    "data": {
        "id": 1,
        "first_name": "Fathur",
        "last_name": "Walkers",
        "email": "fathurwalkers@gmail.com",
        "phone": "085342072402"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Email is not valid format"
}
```

## Update Contact API 
Endpoint : PUT /api/contacts/:id

Headers : 
- Authorization : token

Request Body : 
```json 
{
    "first_name": "Fathur",
    "last_name": "Walkers",
    "email": "fathurwalkers@gmail.com",
    "phone": "085342072402"
}
```

Request Body Success : 
```json 
{
    "data": {
        "id": 1,
        "first_name": "Fathur",
        "last_name": "Walkers",
        "email": "fathurwalkers@gmail.com",
        "phone": "085342072402"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Email is not valid format"
}
```

## Get Contact API 
Endpoint : GET /api/contacts/:id

Headers : 
- Authorization : token

Request Body Success : 
```json 
{
    "data": {
        "id": 1,
        "first_name": "Fathur",
        "last_name": "Walkers",
        "email": "fathurwalkers@gmail.com",
        "phone": "085342072402"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Contact is not found"
}
```

## Search Contact API 
Endpoint : GET /api/contacts

Headers : 
- Authorization : token

Query Parameters : 
- name : Search by first_name or last_name, using LIKE, optional
- email : Search by email, using LIKE, optional
- phone : number of page, default 1
- page : size of page, default 10

Request Body Success : 
```json 
{
    "data": [
        {
            "id": 1,
            "first_name": "Fathur",
            "last_name": "Walkers",
            "email": "fathurwalkers@gmail.com",
            "phone": "085342072402"
        },
        {
            "id": 2,
            "first_name": "Awal",
            "last_name": "Rajab",
            "email": "awalrajab@gmail.com",
            "phone": "08492929192"
        }
    ],
    "paging": {
        "page": 1,
        "total_page": 3,
        "total_item": 30,
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Unauthorized"
}
```


## Remove Contact API 
Endpoint : DELETE /api/contacts/:id

Headers : 
- Authorization : token

Request Body Success : 
```json 
{
    "data": "OK"
}
```

Request Body Error : 
```json 
{
    "errors": "Contact is not found"
}
```







