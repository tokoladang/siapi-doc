# [Buyer] Keranjang

<aside class="notice">
membutuhkan Autentikasi/Token <strong>buyer</strong>.
</aside>

## Get Keranjang Belanja

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/carts"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```
> Contoh Json Response :

```json
[
  {
    "cart_items": [
      {
        "cart_id": "integer",
        "created_at": "datetime",
        "id": "integer",
        "price": "integer",
        "product": {"id": "integer", "name": "Keyboard HP", "price": "integer",…},
        "product_id": "integer",
        "quantity": "integer",
        "selected": "boolean",
        "shipping": "json",
        "tax_price": "integer",
        "total_price": "integer",
        "updated_at": "datetime"
      }
    ],
    "created_at": "datetime",
    "funding_source": "json",
    "id": "integer",
    "merchant": {"id": "integer", "name": "string", "slug": "string", "status": "string", "image": "string"},
    "merchant_id": "integer",
    "school_id": "string",
    "selected": "boolean",
    "shipping": "json",
    "shipping_address": {"from": "string", "thru": "string"},
    "shipping_list": "json",
    "updated_at": "datetime"
  }
]
```
endpoint ini digunakan untuk mendapatkan data keranjang belanja.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts`

## Post Tambah Barang Ke Keranjang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/add"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "product_id": "integer",
        "quantity": "integer"
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk menambahkan barang ke keranjang belanja.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/add`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
product_id | integer | true | Id Produk    
quantity | integer | true | Jumlah

## Post Ubah Data Keranjang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/update-cart"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "type": "string",
        "cart_id": "integer",
        "selected": "boolean"
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk memperbarui data keranjang belanja.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/update-cart`

### Query Body

| Parameter    | Default | required | Deskripsi                                           
| ------------ | ------- | -------- | ----------------------------------------
| type         | string  | true     | Tipe data yang di update `select,remove` 
| cart_id      | integer | true     | Id keranjang  
| selected     | boolean | true if type = `select` | true / false

## Post Ubah Barang Di Keranjang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/update-item"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "type": "string",
        "cart_item_id": "integer",
        "quantity": "integer",
        "selected": "boolean",
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk merubah item barang di keranjang belanja.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/update-item`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
type | string | true | Tipe
cart_item_id | integer | true | Id item di keranjang
quantity | integer | true if type `quantity` | jumlah
selected | boolean | true if type `select` | true / false

## Get Data Biaya Pengiriman

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/refresh-shipping"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk mendapatkan data biaya pengiriman.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/refresh-shipping`

## Post Pilih Pengiriman

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/pick-shipping"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "cart_id": "integer",
        "service": "string"
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk memilih pengiriman.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/pick-shipping`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
cart_id | integer | true | Id keranjang
service | string | true | Jasa pengiriman

## Post Perbarui Pengiriman

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/update-funding"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "cart_id": "integer",
        "funding_source": {
          "code": "string",
          "name": "string",
          "year": "integer"
        }
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk memilih pengiriman.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/update-funding`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
cart_id | integer | true | Id keranjang
funding_source.code | string | true | Kode
funding_source.name | string | true | Nama
funding_source.year | integer | true | Tahun

## Post Checkout Pesanan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/checkout"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "note": "string",
        "nego": "boolean"
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk checkout pesanan.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/checkout`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
note | string | true | Catatan
nego | integer | true | Nego / Proses
