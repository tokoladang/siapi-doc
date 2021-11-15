# [Seller] Produk

Product digunakan untuk mengambil data Produk toko, membuat data produk toko, mengupdate data produk toko, dan merubah status produk toko.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## DATA Produk

## Get Semua Produk Toko

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products?q=&status=&page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
[
  {
    "id": "integer",
    "availability_status": "string",
    "kind": "string",
    "name": "string",
    "price": "integer",
    "qty_available": "integer",
    "status": "string",
    "taxed": "boolean"
  }
]

```
endpoint ini digunakan untuk mendapatkan data semua Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci pencarian
status | string | false | Kata kunci status
page | string | false | Halaman

## Get Produk Detail

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/{id}"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

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
endpoint ini digunakan untuk mendapatkan data detail Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/{id}`

## Get Jumlah Produk

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/item/total"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
{
  "total": "integer", 
  "available": "1"
}

```
endpoint ini digunakan untuk mendapatkan data jumlah Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/item/total`

## Get cari produk buku

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/book/search?q=&type=&page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
[
  {
    "author": "string",
    "category_id": "integer",
    "category_is_leaf": "boolean",
    "category_path": "string",
    "class": "string",
    "classification": "string",
    "description": "string",
    "edition": "integer",
    "id": "string",
    "isbn": "string",
    "physical_description": {},
    "prices": [],
    "publication_year": "integer",
    "publisher": "string",
    "school_level": "string",
    "subject": "string",
    "synopsis": "string",
    "title": "string"
  }
]

```
endpoint ini digunakan untuk mendapatkan data Produk buku.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/book/search?q=&type=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci pencarian
status | string | false | Kata kunci status
page | string | false | Halaman

## Get detail produk buku

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/book/{id}"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json

{
  "author": "string",
  "category_id": "integer",
  "category_is_leaf": "boolean",
  "category_path": "string",
  "class": "string",
  "classification": "string",
  "description": "string",
  "edition": "integer",
  "id": "string",
  "isbn": "string",
  "physical_description": {},
  "prices": [],
  "publication_year": "integer",
  "publisher": "string",
  "school_level": "string",
  "subject": "string",
  "synopsis": "string",
  "title": "string"
}

```
endpoint ini digunakan untuk mendapatkan data detail Produk buku.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/book/{id}`

## Get Ulasan Produk

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/{id}/reviews"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "customer_order_item_id": "integer",
    "id": "integer",
    "message": "string",
    "product_id": "string",
    "rating": "integer",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "updated_at": "datetime"
  }
]

```
endpoint ini digunakan untuk mendapatkan data ulasan Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/book/{id}/reviews`

## Get diskusi produk

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/{id}/discussion?page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json

[
  {
    "created_at": "datetime",
    "created_by": "string",
    "customer_id": "integer",
    "id": "integer",
    "merchant_discuss_replies": [
      {"id": "integer", "merchant_discuss_id": "integer", "customer_id": "integer", "school_id": "integer", "message": "string"}
    ],
    "merchant_id": "integer",
    "message": "string",
    "product_id": "integer",
    "school": {"id": "string", "name": "string"},
    "school_id": "string",
    "updated_at": "datetime",
    "updated_by": "string"
  }
]

```
endpoint ini digunakan untuk mendapatkan data diskusi Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/book/{id}/discussion?page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
page | string | false | Halaman

## Post balas diskusi produk

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/products/{discussId}/discussion-reply"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json

{
  "created_at": "datetime",
  "id": "integer",
  "merchant_discuss_id": "integer",
  "message": "string",
  "updated_at": "datetime"
}

```
endpoint ini digunakan untuk membalas diskusi Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/book/{id}/discussion-reply`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | string | true | Pesan

## Post Tambah Produk baru

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/products"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "kind": "string",
        "name": "string",
        "description": "string",
        "product_category_id": "integer",
        "image": "string",
        "images": [],
        "price": "integer",
        "price_zone_1": "integer",
        "price_zone_2": "integer",
        "price_zone_3": "integer",
        "price_zone_4": "integer",
        "price_zone_5": "integer",
        "wholesales": "[{"quantity": "integer", "price": "integer"}]",
        "discount": "integer",
        "taxed": "boolean",
        "qty_available": "integer",
        "weight": "integer",
        "is_secondhand": "boolean",
        "isbn": "string",
        "with_shipping_cost": "boolean",
        "merchant_storage_id": "integer",
        "is_umkm": "boolean",
        "is_domestic": "boolean",
        "availability_status": "string",
        "dimension": "{"l": "integer", "w": "integer", "h": "integer"}",
        "min_order": "integer",
        "brand": "string",
        "warranty": "string",
        "guaranty": "string",
        "is_kemdikbud": "boolean",
        "catalogue_id": "string",
        "classification_catalogue": "string",
      }'
```
> Contoh Json Response :

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
endpoint ini digunakan untuk membuat data produk baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
kind | string | true | Jenis Produk (Non Buku/Buku/Jasa)
name | string | true | Nama Produk
description | string | true | Deskripsi Produk
product_category_id | integer | true | Kategori Produk
image | string | false | Foto Produk
images | array | false | Foto Produk
price | integer | true | Harga Utama
price_zone_1 | integer | true | Harga menurut zona 1
price_zone_2 | integer | true | Harga menurut zona 2
price_zone_3 | integer | true | Harga menurut zona 3
price_zone_4 | integer | true | Harga menurut zona 4
price_zone_5 | integer | true | Harga menurut zona 5
wholesales | array | true | Harga grosir
discount | integer | true | Diskon
taxed | boolean | true | Apakah produk kena pajak?
qty_available | integer | true | Jumlah Produk
weight | integer | true | Berat produk
is_secondhand | boolean | true | Apakah produk tangan kedua?
isbn | string | true if kind=Buku | Nomor isbn buku
with_shipping_cost | boolean | true | Apakah dengan biaya pengiriman?
merchant_storage_id | integer | false | IEtalase
is_umkm | boolean | true | Apakah termasuk usaha umkm?
is_domestic | boolean | true | Apakah termasuk produk domestik?
availability_status | string | true | Tersedia / Preorder
dimension | json | true | Dimensi Produk
min_order | integer | true | Minimal Pembelian
brand | string | false | Merk
warranty | string | false | garansi produk
guaranty | string | false | garansi pengiriman
is_kemdikbud | boolean | true | Apakah produk Kemdikbud?
catalogue_id | string | true if kind=buku | id katalog buku
classification_catalogue | string | false | klasifikasi id katalog buku

## Put Ubah Data Produk

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/products/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "kind": "string",
        "name": "string",
        "description": "string",
        "product_category_id": "integer",
        "image": "string",
        "images": [],
        "price": "integer",
        "price_zone_1": "integer",
        "price_zone_2": "integer",
        "price_zone_3": "integer",
        "price_zone_4": "integer",
        "price_zone_5": "integer",
        "wholesales": "[{"quantity": "integer", "price": "integer"}]",
        "discount": "integer",
        "taxed": "boolean",
        "qty_available": "integer",
        "weight": "integer",
        "is_secondhand": "boolean",
        "isbn": "string",
        "with_shipping_cost": "boolean",
        "merchant_storage_id": "integer",
        "is_umkm": "boolean",
        "is_domestic": "boolean",
        "availability_status": "string",
        "dimension": "{"l": "integer", "w": "integer", "h": "integer"}",
        "min_order": "integer",
        "brand": "string",
        "warranty": "string",
        "guaranty": "string",
        "is_kemdikbud": "boolean",
        "catalogue_id": "string",
        "classification_catalogue": "string",
      }'
```
> Contoh Json Response :

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
endpoint ini digunakan untuk merubah data produk.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/products/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
kind | string | true | Jenis Produk (Non Buku/Buku/Jasa)
name | string | true | Nama Produk
description | string | true | Deskripsi Produk
product_category_id | integer | true | Kategori Produk
image | string | false | Foto Produk
images | array | false | Foto Produk
price | integer | true | Harga Utama
price_zone_1 | integer | true | Harga menurut zona 1
price_zone_2 | integer | true | Harga menurut zona 2
price_zone_3 | integer | true | Harga menurut zona 3
price_zone_4 | integer | true | Harga menurut zona 4
price_zone_5 | integer | true | Harga menurut zona 5
wholesales | array | true | Harga grosir
discount | integer | true | Diskon
taxed | boolean | true | Apakah produk kena pajak?
qty_available | integer | true | Jumlah Produk
weight | integer | true | Berat produk
is_secondhand | boolean | true | Apakah produk tangan kedua?
isbn | string | true if kind=Buku | Nomor isbn buku
with_shipping_cost | boolean | true | Apakah dengan biaya pengiriman?
merchant_storage_id | integer | false | IEtalase
is_umkm | boolean | true | Apakah termasuk usaha umkm?
is_domestic | boolean | true | Apakah termasuk produk domestik?
availability_status | string | true | Tersedia / Preorder
dimension | json | true | Dimensi Produk
min_order | integer | true | Minimal Pembelian
brand | string | false | Merk
warranty | string | false | garansi produk
guaranty | string | false | garansi pengiriman
is_kemdikbud | boolean | true | Apakah produk Kemdikbud?
catalogue_id | string | true if kind=buku | id katalog buku
classification_catalogue | string | false | klasifikasi id katalog buku

## Put Ubah Status Produk

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/products/{id}/status"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "status" : "string",
      }'
```
> Contoh Json Response :

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
endpoint ini digunakan untuk mengubah status produk toko.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/products/{id}/status`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | string | true | status produk

## Expor Data Produk

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/document/export?page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "page" => "integer"
      }'
```

> Contoh Json Response :

```json
"File Excel"

```
endpoint ini digunakan untuk mendapatkan data jumlah Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/document/export?page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
page | integer | true | setiap halaman max. 500 data

## Impor Data Produk

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products/document/import"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "file" => "file",
        "type" => "string"
      }'
```

> Contoh Json Response :

```json
{
  "id": "integer",
  "merchant_id": "integer",
  "type": "string",
  "done": "boolean",
  "note": "string",
  "uploaded": "string",
  "downloadable": "string",
  "created_at": "datetime",
  "updated_at": "datetime"
}

```
endpoint ini digunakan untuk mendapatkan data jumlah Produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products/document/import`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
file | file | true | file excel
type | string | true | tipe
