# [Buyer] Ikuti Toko

## Get Data Toko Diikuti

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/favourite/merchant"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "merchant_id": "integer",
    "school_id": "string",
    "created_by": "string",
    "updated_by": "string",
    "created_at": "datetime",
    "updated_at": "datetime"
  }
]
```

endpoint ini digunakan untuk mendapatkan data toko yang di ikuti.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/favourite/merchant`

## Post Ikuti Toko

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/favourite/merchant"
-H 'Content-Type: application/json'
-d '{
      "merchant_id": "integer"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk mengikuti toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/favourite/merchant`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
merchant_id | integer | true | Id Toko

## Delete Unfollow Toko

> jenis: buyer

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/buyer/favourite/merchant/{id}"
-H 'Content-Type: application/json'
-d '{
      "merchant_id": "integer"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk berhenti mengikuti toko.

### HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/buyer/favourite/merchant/{id}`
