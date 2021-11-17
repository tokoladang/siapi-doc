# [Admin] Sekolah

## Get Semua Sekolah

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/schools?q=&status=&page"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "admin_note": "string",
    "city_id": "integer",
    "created_at": "datetime",
    "details": {"sekolah_id": "string", "nama_sekolah": "string", "status": "string",...},
    "district_id": "integer",
    "email_verified_at": "datetime",
    "funding_sources": [{"id": "string", "code": "string", "name": "string", "year": "integer",...}],
    "id": "string",
    "image": "string",
    "name": "string",
    "province_id": "integer",
    "suspended": "boolean",
    "type": "string",
    "updated_at": "datetime",
    "zone": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan semua data sekolah.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/schools?q=&status=&page`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Get Detail Sekolah

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/schools/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "admin_note": "string",
  "city_id": "integer",
  "created_at": "datetime",
  "details": {"sekolah_id": "string", "nama_sekolah": "string", "status": "string",...},
  "district_id": "integer",
  "email_verified_at": "datetime",
  "funding_sources": [{"id": "string", "code": "string", "name": "string", "year": "integer",...}],
  "id": "string",
  "image": "string",
  "name": "string",
  "province_id": "integer",
  "suspended": "boolean",
  "type": "string",
  "updated_at": "datetime",
  "zone": "string"
}
```

endpoint ini digunakan untuk mendapatkan detail data sekolah.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/schools/{id}`


## Post Blokir Sekolah

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/schools/suspend"
-H 'Content-Type: application/json'
-d '{
      "id": "string",
      "note": "string"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk memblokir sekolah.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/schools/suspend`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | string | true | Id Sekolah
note | string | true | Catatan


## Post Aktifkan Sekolah

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/schools/unsuspend"
-H 'Content-Type: application/json'
-d '{
      "id": "string"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk aktifkan sekolah.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/schools/unsuspend`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | string | true | Id Sekolah

## Get User Sekolah

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/customers/{schoolId}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string",
    "email": "string",
    "suspended": "boolean",
    "school_id": "string",
    "details": "json",
    "created_at": "datetime",
    "updated_at": "datetime"
  }
]
```

endpoint ini digunakan untuk mendapatkan data users berdasarkan id sekolah.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/customers/{schoolId}`

## Get User Detail

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/customers/{id}/detail"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "id": "integer",
  "name": "string",
  "email": "string",
  "suspended": "boolean",
  "school_id": "string",
  "details": "json",
  "created_at": "datetime",
  "updated_at": "datetime"
}
```

endpoint ini digunakan untuk mendapatkan data detail user.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/customers/{id}/detail`
