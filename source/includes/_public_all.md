# [Public] Semua

## Get Data Utama

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/home"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "categories": [],
    "merchants": [],
    "products": [],
    "promos": []
  }
]
```

endpoint ini digunakan untuk mendapatkan data Utama.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/home`

## Get Sugesti Pencarian

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/search/suggestion?q="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "merchants": [
    {
      "city": {"id": "integr", "name": "string"},
      "city_id": "string",
      "id": "integer",
      "image": "string",
      "name": "string",
      "slug": "string"
    }
  ],
  "products": [
    {"id": "integer", "name": "string", "slug": "string", "merchant_name": "string", "image": "string"}
  ]
}
```

endpoint ini digunakan untuk mendapatkan data dengan sugesti pencarian.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/search/suggestion?q=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci

## Get Data Metode Pembayaran

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/payment-methods"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "image": "string",
    "name": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data metode pembayaran.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/payment-methods`

## Get Semua Etalse

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/merchant-storages/{merchantId}"
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
    "merchant_id": "integer",
    "name": "string",
    "updated_at": "datetime",
    "updated_by": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data etalse.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/merchant-storages/{merchantId}`

## Get Semua Kategori Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/product-categories?q=&parent="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "created_by": "string",
    "description": "string",
    "enabled": "true",
    "id": "integer",
    "image": "string",
    "level": "integer",
    "name": "string",
    "parent_id": "integer",
    "sequence": "integer",
    "slug": "string",
    "updated_at": "datetime",
    "updated_by": "string",
    "_lft": "integer",
    "_rgt": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data kategori produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/product-categories?q=&parent=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
parent | integer | false | Kategori induk

## Get Turunan Kategori Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/product-categories/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string",
    "parent_id": "integer",
    "slug": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data turunan kategori.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/product-categories/{id}`

## Get Data Bank

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/banks"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data Bank.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/banks`

## Get Data Provinsi

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/provinces"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data provinsi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/provinces`

## Get Data Kota By Provinsi

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/cities/{provincyId}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data kota/kab berdasarkan provinsi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/cities/{provincyId}`

## Get Data Kecamatan By Kota

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/districts/{cityId}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data kecamatan berdasarkan kota.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/districts/{cityId}`

## Get Data Desa By Kecamatan

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/village/{districtId}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "name": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data desa berdasarkan kecamatan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/village/{districtId}`
