# [Public] Produk

## Get Semua Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/products?q=&page=&sort=&cat=&min=&max=&city=&rat=&sc=&domestic=&umkm="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "availability_status": "string",
    "category_name": "string",
    "city_name": "string",
    "description": "string",
    "dimension": {"l": "integer", "w": "integer", "h": "integer"},
    "discount": "integer",
    "id": "integer",
    "image": "string",
    "images": [],
    "merchant_id": "integer",
    "merchant_name": "string",
    "merchant_slug": "string",
    "name": "string",
    "price": "integer",
    "price_zone_1": "integer",
    "price_zone_2": "integer",
    "price_zone_3": "integer",
    "price_zone_4": "integer",
    "price_zone_5": "integer",
    "product_category_id": "integer",
    "province_name": "string",
    "qty_available": "integer",
    "qty_sell": "integer",
    "rating": "string",
    "sku": "string",
    "slug": "string",
    "taxed": "boolean",
    "weight": "integer",
    "with_shipping_cost": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/products?q=&page=&sort=&cat=&min=&max=&city=&rat=&sc=&domestic=&umkm=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
page | integer | false | Halaman
sort | string | false | Sortir
cat | string | false | Kategori
min | string | false | Min. Harga
max | string | false | Max. Harga
city | string | false | Kota
rat | string | false | Rating
sc | string | false | Kondisi
domestic | string | false | Buatan Indo?
umkm | string | false | Produk UMKM?

## Get Detail Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/products/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "availability_status": "string",
  "category_name": "string",
  "city_name": "string",
  "description": "string",
  "dimension": {"l": "integer", "w": "integer", "h": "integer"},
  "discount": "integer",
  "id": "integer",
  "image": "string",
  "images": [],
  "merchant_id": "integer",
  "merchant_name": "string",
  "merchant_slug": "string",
  "name": "string",
  "price": "integer",
  "price_zone_1": "integer",
  "price_zone_2": "integer",
  "price_zone_3": "integer",
  "price_zone_4": "integer",
  "price_zone_5": "integer",
  "product_category_id": "integer",
  "province_name": "string",
  "qty_available": "integer",
  "qty_sell": "integer",
  "rating": "string",
  "sku": "string",
  "slug": "string",
  "taxed": "boolean",
  "weight": "integer",
  "with_shipping_cost": "integer"
}
```

endpoint ini digunakan untuk mendapatkan data detail produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/products/{id}`

## Get Review Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/products/reviews/{id}"
-H 'Content-Type: application/json'
-d '{}'
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

endpoint ini digunakan untuk mendapatkan data ulasan produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/products/reviews/{id}`

## Get Diskusi Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/products/reviews/{id}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "created_by": "string",
    "customer_id": "integer",
    "id": "integer",
    "merchant_discuss_replies": [],
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

endpoint ini digunakan untuk mendapatkan data diskusi produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/products/reviews/{id}`

## Get Produk By Kategori

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/products/category/{categoryId}?page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "availability_status": "string",
    "category_name": "string",
    "city_name": "string",
    "description": "string",
    "dimension": {"l": "integer", "w": "integer", "h": "integer"},
    "discount": "integer",
    "id": "integer",
    "image": "string",
    "images": [],
    "merchant_id": "integer",
    "merchant_name": "string",
    "merchant_slug": "string",
    "name": "string",
    "price": "integer",
    "price_zone_1": "integer",
    "price_zone_2": "integer",
    "price_zone_3": "integer",
    "price_zone_4": "integer",
    "price_zone_5": "integer",
    "product_category_id": "integer",
    "province_name": "string",
    "qty_available": "integer",
    "qty_sell": "integer",
    "rating": "string",
    "sku": "string",
    "slug": "string",
    "taxed": "boolean",
    "weight": "integer",
    "with_shipping_cost": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data produk berdasarkan kategori.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/products/category/{categoryId}?page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
page | integer | false | Halaman

## Get Produk By Toko

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/public/products/category/{categoryId}?q=&page=&etalase=&sort="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "availability_status": "string",
    "category_name": "string",
    "city_name": "string",
    "description": "string",
    "dimension": {"l": "integer", "w": "integer", "h": "integer"},
    "discount": "integer",
    "id": "integer",
    "image": "string",
    "images": [],
    "merchant_id": "integer",
    "merchant_name": "string",
    "merchant_slug": "string",
    "name": "string",
    "price": "integer",
    "price_zone_1": "integer",
    "price_zone_2": "integer",
    "price_zone_3": "integer",
    "price_zone_4": "integer",
    "price_zone_5": "integer",
    "product_category_id": "integer",
    "province_name": "string",
    "qty_available": "integer",
    "qty_sell": "integer",
    "rating": "string",
    "sku": "string",
    "slug": "string",
    "taxed": "boolean",
    "weight": "integer",
    "with_shipping_cost": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data produk berdasarkan toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/public/products/category/{categoryId}?q=&page=&etalase=&sort=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
page | integer | false | Halaman
sort | string | false | Sortir
etalase | string | false | Etalase
