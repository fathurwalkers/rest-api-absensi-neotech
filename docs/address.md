# Address API Specs

## Create Address API 
Endpoint : POST /api/contacts/:contactId/addresses

Headers : 
- Authorization : token

Request Body : 
```json 
{
    "street": "Masukkan nama Jalan",
    "city": "Masukkan nama Kota",
    "province": "Masukkan nama Provinsi",
    "country": "Masukkan nama Negara",
    "postal_code": "Kode Pos"
}
```

Request Body Success : 
```json 
{
    "data": {
        "id": 1,
        "street": "Masukkan nama Jalan",
        "city": "Masukkan nama Kota",
        "province": "Masukkan nama Provinsi",
        "country": "Masukkan nama Negara",
        "postal_code": "Kode Pos"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Country is required"
}
```

## Update Address API 
Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers : 
- Authorization : token

Request Body : 
```json 
{
    "street": "Masukkan nama Jalan",
    "city": "Masukkan nama Kota",
    "province": "Masukkan nama Provinsi",
    "country": "Masukkan nama Negara",
    "postal_code": "Kode Pos"
}
```

Request Body Success : 
```json 
{
    "data": {
        "id": 1,
        "street": "Masukkan nama Jalan",
        "city": "Masukkan nama Kota",
        "province": "Masukkan nama Provinsi",
        "country": "Masukkan nama Negara",
        "postal_code": "Kode Pos"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Country is required"
}
```

## Get Address API 
Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers : 
- Authorization : token

Request Body Success : 
```json 
{
    "data": {
        "id": 1,
        "street": "Masukkan nama Jalan",
        "city": "Masukkan nama Kota",
        "province": "Masukkan nama Provinsi",
        "country": "Masukkan nama Negara",
        "postal_code": "Kode Pos"
    }
}
```

Request Body Error : 
```json 
{
    "errors": "Contact is not found"
}
```

## List Address API 
Endpoint : GET /api/contacts/:contactId/addresses

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
            "street": "Masukkan nama Jalan",
            "city": "Masukkan nama Kota",
            "province": "Masukkan nama Provinsi",
            "country": "Masukkan nama Negara",
            "postal_code": "Kode Pos"
        },
        {
            "id": 2,
            "street": "Masukkan nama Jalan lagi",
            "city": "Masukkan nama Kota lagi",
            "province": "Masukkan nama Provinsi lagi",
            "country": "Masukkan nama Negara lagi",
            "postal_code": "Kode Pos lagi"
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
    "errors": "Contact is not found"
}
```

## Remove Address API 
Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

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
    "errors": "Address is not found"
}
```







