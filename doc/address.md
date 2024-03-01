# Address API Spec

## Create Address

Endpoint : POST /api/contacts/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jl. Buntu",
  "city": "Kota Bawah Tanah",
  "province": "Privinsi",
  "country": "Negara Apa",
  "postal_code": "180997"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Buntu",
    "city": "Kota Bawah Tanah",
    "province": "Privinsi",
    "country": "Negara Apa",
    "postal_code": "180997"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Postal Code is Required!"
}
```

## Get Address

Endpoint : GET /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Buntu",
    "city": "Kota Bawah Tanah",
    "province": "Privinsi",
    "country": "Negara Apa",
    "postal_code": "180997"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Address is not found!"
}
```

## Update Address

Endpoint : PUT /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jl. Buntu",
  "city": "Kota Bawah Tanah",
  "province": "Privinsi",
  "country": "Negara Apa",
  "postal_code": "180997"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Buntu",
    "city": "Kota Bawah Tanah",
    "province": "Privinsi",
    "country": "Negara Apa",
    "postal_code": "180997"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Postal Code is Required!"
}
```

## Remove Address

Endpoint : DELETE /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
{
  "errors": "Address is not found!"
}
```

## List Address

Endpoint : GET /api/contacts/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jl. Buntu",
      "city": "Kota Bawah Tanah",
      "province": "Privinsi",
      "country": "Negara Apa",
      "postal_code": "180997"
    },
    {
      "id": 2,
      "street": "Jl. Buntu",
      "city": "Kota Bawah Tanah",
      "province": "Privinsi",
      "country": "Negara Apa",
      "postal_code": "180997"
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "errors": "Contact is not found!"
}
```
