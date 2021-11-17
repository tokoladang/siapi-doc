# [Admin] Complain

## Get Semua Komplain

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/complains?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "code": "string",
    "created_at": "datetime",
    "created_by": "string",
    "customer_order": {"id": "integer", "order_no": "string"},
    "customer_order_id": "integer",
    "from": "string",
    "id": "integer",
    "merchant": {"id": "integer", "name": "string"},
    "merchant_id": "integer",
    "message": "string",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "status": "string",
    "title": "string",
    "updated_at": "datetime",
    "updated_by": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/complains?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Get Riwayat Komplain

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/complains/{complainId}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "created_by": "string",
    "id": "integer",
    "merchant_complain_id": "integer",
    "message": "string",
    "role": "string",
    "sender": {"id": "integer", "merchant_id": "integer"},
    "updated_at": "datetime",
    "updated_by": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data riwayat Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/complains/{complainId}`

## POST Menanggapi Komplain

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/complains/{complain}/reply"
-H 'Content-Type: application/json'
-d '{
      "message": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk menanggapi pesan pada komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/complains/{complain}/reply`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan

## POST Menutup Komplain

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/complains/{complain}/close"
-H 'Content-Type: application/json'
-d '{
      "message": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk menutup pesan pada komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/complains/{complain}/close`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan

## POST Eskalasi Komplain

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/complains/{complain}/escalate"
-H 'Content-Type: application/json'
-d '{
      "message": "string"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk eskalasi komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/complains/{complain}/escalate`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan
