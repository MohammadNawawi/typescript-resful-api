# Contact API Spec

## Create Contact

Endpoint : POST /api/contacts

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "first_name": "Mohammad",
  "last_name": "Nawawi",
  "email": "mohammadnawawi@fromnaw.com",
  "phone": "0123456789"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "first_name": "Mohammad",
    "last_name": "Nawawi",
    "email": "mohammadnawawi@fromnaw.com",
    "phone": "0123456789"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Email is required!"
}
```

## Get Contact

Endpoint : GET /api/contacts/:id

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "first_name": "Mohammad",
    "last_name": "Nawawi",
    "email": "mohammadnawawi@fromnaw.com",
    "phone": "0123456789"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Contact is not found!"
}
```

## Update Contact

Endpoint : PUT /api/contacts

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "first_name": "Mohammad",
  "last_name": "Nawawi",
  "email": "mohammadnawawi@fromnaw.com",
  "phone": "0123456789"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "first_name": "Mohammad",
    "last_name": "Nawawi",
    "email": "mohammadnawawi@fromnaw.com",
    "phone": "0123456789"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Email is required!"
}
```

## Remove Contact

Endpoint : DELETE /api/contacts/:id

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "first_name": "Mohammad",
  "last_name": "Nawawi",
  "email": "mohammadnawawi@fromnaw.com",
  "phone": "0123456789"
}
```

Response Body (Success) :

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
{
  "errors": "Contact is not found!"
}
```

## Search Contact

Endpoint : POST /api/contacts

Query Parameter :

- name : string, contact name or contact last name, optional
- phone : string, contact phone, optional
- email : string, contact email, optional
- page : number, default 1
- size : number. default 10

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Mohammad",
      "last_name": "Nawawi",
      "email": "mohammadnawawi@fromnaw.com",
      "phone": "0123456789"
    },
    {
      "id": 2,
      "first_name": "Mohammad",
      "last_name": "Nawawi",
      "email": "mohammadnawawi@fromnaw.com",
      "phone": "0123456789"
    }
  ],
  "paging": {
    "current_page": 1,
    "total_page": 10,
    "size": 10
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized!"
}
```
