# [Buyer] Perbandingan

## Get Daftar Perbandingan

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/compares?status=&page="
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
    "funding_source": {"kode_sumber_dana": "string", "sumber_dana": "string"},
    "id": "integer",
    "is_used": "boolean",
    "school_id": "string",
    "updated_at": "datetime",
    "updated_by": "string"
  }
]
```

endpoint ini digunakan untuk mendapatkan data perbandingan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/compares?status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | string | false | Status
page | integer | false | Halaman

## Get Daftar Perbandingan By Grup

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/compares/{compareId}/group"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "all_responded": "boolean",
  "groups": [
    {
      "compare_id": "integer",
      "compare_items": [{"id": "integer", "compare_group_id": "integer", "product_id": "integer", "quantity": "integer",…}],
      "courier": {"name": "string", "cost": "integer", "etd": "string"},
      "courier_name": "string",
      "id": "integer",
      "merchant": {"id": "integer", "slug": "lina-com-11019", "name": "string",…},
      "merchant_id": "integer",
      "shipping_cost": "integer",
      "status": "boolean",
      "tax_price": "integer",
      "time_limit": "integer",
      "total_price": "integer",
      "total_qty": "integer",
      "total_weight": 0"integer"
    }
  ],
  "interval": "integer"
}
```

endpoint ini digunakan untuk mendapatkan data perbandingan berdasarkan grup.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/compares/{compareId}/group`

## Post Perbandingan Baru

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/compares/new"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "code": "string",
      }'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```
endpoint ini digunakan untuk menambahkan perbandingan barang.

`POST https://staging.siapi.tokoladang.co.id/buyer/compares/new`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | ---------
code | string | true | Kode 

## Put Ubah Perbandingan

> jenis: buyer

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/buyer/compares/{id}/update"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "code": "string",
      }'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```

endpoint ini digunakan untuk update data perbandingan barang.

`PUT https://staging.siapi.tokoladang.co.id/buyer/compares/{id}/update`

### Query Body

| Parameter | Default | required | Deskripsi |
| --------- | ------- | -------- | --------- |
| code | string | true | Kode

## Delete Hapus Perbandingan

> jenis: buyer

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/buyer/compares/{id}/remove"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```

endpoint ini digunakan untuk menghapus perbandingan barang.

`DELETE https://staging.siapi.tokoladang.co.id/buyer/compares/{id}/remove`

## Post Tambah Produk Ke Perbandingan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/compares/{id}/add"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "type": "string",
        "id": "integer"
      }'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```
endpoint ini digunakan untuk menambahkan produk ke perbandingan yang sudah ada.

`POST https://staging.siapi.tokoladang.co.id/buyer/compares/{id}/add`

### Query Body

Parameter | Default | required | Deskripsi 
--------- | ------- | -------- | --------- 
type | string | true | Tipe 
id | integer | true | Kode 


## Delete Hapus Grup Dari Perbandingan

> jenis: buyer

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/buyer/compares/group/{group}/remove"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```

endpoint ini digunakan untuk menghapus produk dari perbandingan.

`DELETE https://staging.siapi.tokoladang.co.id/buyer/compares/group/{group}/remove`

## Post Simpan Perbandingan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/compares"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "code" => "string",
        "funding_source" => "json",
        "groups" : {
          "merchant_id": "integer",
          "total_qty": "integer",
          "total_price": "integer",
          "tax_price": "integer",
          "total_weight": "integer",
          "shipping": "integer",
          "shipping_address": "string",
          compare_items: {
            "product_id": "integer",
            "product_name": "string",
            "product_image": "string",
            "quantity": "integer",
            "price": "integer",
            "total_price": "integer",
            "tax_price": "integer",
            "shipping": "json"
          }
        }
      }'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```
endpoint ini digunakan untuk menyimpan data perbandingan.

`POST https://staging.siapi.tokoladang.co.id/buyer/compares`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | ---------
code | string | true | Kode 
funding_source | json | true | Sumber dana
groups.merchant_id | integer | true | Id Toko
groups.total_qty | integer | true | Jumlah produk
groups.total_price | integer | true | Harga
groups.tax_price | integer | true | Pajak
groups.total_weight | integer | true | Berat
groups.shipping | json | true | Pengiriman
groups.shipping_address | string | true | Alamat pengiriman
groups.compare_items.product_id | integer | true | Id Produk
groups.compare_items.product_name | string | true | Nama produk
groups.compare_items.product_image | string | true | Gambar produk
groups.compare_items.quantity | integer | true | Jumlah /produk
groups.compare_items.price | integer | true | Harga /produk
groups.compare_items.total_price | integer | true | Total harga
groups.compare_items.tax_price | integer | true | Pajak
groups.compare_items.shipping | json | false | Pengiriman

## Post Ubah Perbandingan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/compares/update"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "id" => "integer",
        "code" => "string",
        "funding_source" => "json",
        "groups" : {
          "merchant_id": "integer",
          "total_qty": "integer",
          "total_price": "integer",
          "tax_price": "integer",
          "total_weight": "integer",
          "shipping": "integer",
          "shipping_address": "string",
          compare_items: {
            "product_id": "integer",
            "product_name": "string",
            "product_image": "string",
            "quantity": "integer",
            "price": "integer",
            "total_price": "integer",
            "tax_price": "integer",
            "shipping": "json"
          }
        }
      }'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```
endpoint ini digunakan untuk merubah data perbandingan.

`POST https://staging.siapi.tokoladang.co.id/buyer/compares/update`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | ---------
id | integer | true | Id Perbandingan 
code | string | true | Kode 
funding_source | json | true | Sumber dana
groups.merchant_id | integer | true | Id Toko
groups.total_qty | integer | true | Jumlah produk
groups.total_price | integer | true | Harga
groups.tax_price | integer | true | Pajak
groups.total_weight | integer | true | Berat
groups.shipping | json | true | Pengiriman
groups.shipping_address | string | true | Alamat pengiriman
groups.compare_items.product_id | integer | true | Id Produk
groups.compare_items.product_name | string | true | Nama produk
groups.compare_items.product_image | string | true | Gambar produk
groups.compare_items.quantity | integer | true | Jumlah /produk
groups.compare_items.price | integer | true | Harga /produk
groups.compare_items.total_price | integer | true | Total harga
groups.compare_items.tax_price | integer | true | Pajak
groups.compare_items.shipping | json | false | Pengiriman

## Post Checkout Dari Perbandingan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/compares/{group}/checkout"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "note" => "string"
      }'
```
> Contoh Json Response :

```json
{
  "compare_id": "code",
  "courier_name": "message"
}
```
endpoint ini digunakan untuk checkout dari perbandingan.

`POST https://staging.siapi.tokoladang.co.id/buyer/compares/{group}/checkout`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | ---------
note | string | true | Catatan
