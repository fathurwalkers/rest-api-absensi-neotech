# User API Specs

## Register User API 
Endpoint : POST /api/users

Request Body : 
```json 
{
    "username": "fathur",
    "password": "jancok",
    "name": "Fathur Walkers",
}
```

Request Body Success : 
```json 
{
    "data": {
        "username": "fathur",
        "name": "Fathur Walkers",
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Username is already registered"
}
```

## Login User API 
Endpoint : POST /api/users/login

Request Body : 
```json 
{
    "username": "fathur",
    "password": "jancok",
}
```

Request Body Success : 
```json 
{
    "data": {
        "token": "unique-token"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Username or password is wrong"
}
```

## Update User API 
Endpoint : PATCH /api/users/current

Headers : 
- Authorization : token

Request Body : 
```json 
{
    "name": "Fathur Walkers Lagi", // Optional 
    "password": "new password", // Optional 
}
```

Request Body Success : 
```json 
{
    "data": {
        "username": "fathur",
        "name": "Fathur Walkers Lagi", // Optional 
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Name length max 100"
}
```

## Get User API 
Endpoint : GET /api/users/current

Headers : 
- Authorization : token

Request Body Success : 
```json 
{
    "data": {
        "username": "fathur",
        "name": "Fathur Walkers Lagi", // Optional 
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Unauthorized"
}
```

## Logout  User API 
Endpoint : DELETE /api/users/logout

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
    "errors": "Unauthorized"
}
```














