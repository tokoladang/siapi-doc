# [Admin]Produk

## Get semua Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```

Contoh Json Response :

```json
[
  {
    "admin_note": "string",
    "availability_status": "string",
    "brand": "string",
    "catalogue_id": "string",
    "categories": [{"id": "integer", "name": "string"}],
    "classification_catalogue": "string",
    "created_at": "datetime",
    "created_by": "string",
    "description": "string",
    "dimension": {"l": "integer", "w": "integer", "h": "integer"},
    "discount": "integer",
    "guaranty": "string",
    "id": "integer",
    "image": "string",
    "images": "array",
    "is_domestic": "boolean",
    "is_kemdikbud": "boolean",
    "is_secondhand": "boolean",
    "is_umkm": "boolean",
    "isbn": "string",
    "kind": "string",
    "merchant_id": "integer",
    "merchant_storage_id": "integer",
    "min_order": "integer",
    "name": "string",
    "power": "integer",
    "price": "integer",
    "price_zone_1": "integer",
    "price_zone_2": "integer",
    "price_zone_3": "integer",
    "price_zone_4": "integer",
    "price_zone_5": "integer",
    "product_category_id": "integer",
    "product_upload_id": "integer",
    "qty_available": "integer",
    "qty_sell": "integer",
    "qualified": "boolean",
    "rating": "string",
    "review_count": "integer",
    "review_total": "integer",
    "sku": "string",
    "slug": "string",
    "status": "string",
    "taxed": "boolean",
    "updated_at": "datetime",
    "updated_by": "string",
    "verified_at": "datetime",
    "verified_by": "string",
    "warranty": "string",
    "weight": "integer",
    "wholesales": [{"quantity": "integer", "price": "integer"}],
    "with_shipping_cost": "boolean"
  }
]
```

endpoint ini digunakan untuk mendapatkan data produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products?q=&status=`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata Kunci Pencarian
status | string | false | Status
page | integer | false | Halaman

## Get Detail Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products/{id}"
-H 'Content-Type: application/json'
-d '{}'
```

Contoh Json Response :

```json
{
  "admin_note": "string",
  "availability_status": "string",
  "brand": "string",
  "catalogue_id": "string",
  "categories": [{"id": "integer", "name": "string"}],
  "classification_catalogue": "string",
  "created_at": "datetime",
  "created_by": "string",
  "description": "string",
  "dimension": {"l": "integer", "w": "integer", "h": "integer"},
  "discount": "integer",
  "guaranty": "string",
  "id": "integer",
  "image": "string",
  "images": "array",
  "is_domestic": "boolean",
  "is_kemdikbud": "boolean",
  "is_secondhand": "boolean",
  "is_umkm": "boolean",
  "isbn": "string",
  "kind": "string",
  "merchant_id": "integer",
  "merchant_storage_id": "integer",
  "min_order": "integer",
  "name": "string",
  "power": "integer",
  "price": "integer",
  "price_zone_1": "integer",
  "price_zone_2": "integer",
  "price_zone_3": "integer",
  "price_zone_4": "integer",
  "price_zone_5": "integer",
  "product_category_id": "integer",
  "product_upload_id": "integer",
  "qty_available": "integer",
  "qty_sell": "integer",
  "qualified": "boolean",
  "rating": "string",
  "review_count": "integer",
  "review_total": "integer",
  "sku": "string",
  "slug": "string",
  "status": "string",
  "taxed": "boolean",
  "updated_at": "datetime",
  "updated_by": "string",
  "verified_at": "datetime",
  "verified_by": "string",
  "warranty": "string",
  "weight": "integer",
  "wholesales": [{"quantity": "integer", "price": "integer"}],
  "with_shipping_cost": "boolean"
}
```

endpoint ini digunakan untuk mendapatkan data detail produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products/{id}`

## Post Verifikasi Produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/products/verify"
-H 'Content-Type: application/json'
-d '{
      "id": "integer",
      "verified": "boolean",
      "status": "string"
    }'
```

Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk verifikasi produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/products/verify`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | integer | true | Id produk
verified | boolean | true | Jika false produk bermasalah
note | string | false | Catatan


## Post Blokir Produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/products/suspend"
-H 'Content-Type: application/json'
-d '{
      "id": "integer",
      "note": "string"
    }'
```

Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk memblokir produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/products/suspend`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | integer | true | Id produk
note | string | false | Catatan


## Post Aktifkan Produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/products/unsuspend"
-H 'Content-Type: application/json'
-d '{
      "id": "integer"
    }'
```

Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk aktifkan kembali produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/products/unsuspend`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | integer | true | Id produk
