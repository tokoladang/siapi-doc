# [Seller] Product

Product digunakan untuk mengambil data Produk toko, membuat data produk toko, mengupdate data produk toko, dan merubah status produk toko.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## Get Semua Produk Toko

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/products"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
{
  "id": 304,
        "sku": "SKU5FEC2EFBA8C4B",
        "name": "barang Baru",
        "description": "Deskripsi Barang Baru",
        "product_category_id": 2,
        "wholesales": [
            "{quantity: 10,price: 9900},{quantity: 20,price: 9800}"
        ],
        "image": "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg",
        "kind": "Non Buku",
}
```
endpoint ini digunakan untuk mendapatkan data Produk toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/products`

## Post Tambah data Produk Toko

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/products"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "kind": "Buku",
        "name": "Arwana Biru",
        "description": "Deskripsi Barang Buku",
        "product_category_id": "2",
        "image": "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg",
        "images": [
            "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg",
            "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg"
        ],
        "price": "10000",
        "price_zone_1": "11000",
        "price_zone_2": "12000",
        "price_zone_3": "13000",
        "price_zone_4": "14000",
        "price_zone_5": "15000",
        "wholesales": [
            {
                "quantity": 10,
                "price": 9900
            },
            {
                "quantity": 20,
                "price": 9800
            }
        ],
        "discount": "1",
        "taxed": "1",
        "qty_available": "5",
        "weight": "1500",
        "is_secondhand": "0",
        "with_shipping_cost": "1",
        "merchant_storage_id": null,
        "is_goods": "1",
        "is_umkm": "1",
        "is_domestic": "1",
        "isbn": "456165216884"
      }'
```

endpoint ini digunakan untuk membuat data produk toko,
membutuhkan isbn apabila kind = Buku.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/products`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
kind | Non Buku/Buku | true | Termasuk buku atau bukan
name |  | true | Nama barang
description |  | true | Deskripsi barang
product_category_id |  | true | Id kategori product
image |  | false | path Gambar
images |  | false | path Gambar
price |  | true | Harga Awal
price_zone_1 |  | true | Harga menurut zona 1
price_zone_2 |  | true | Harga menurut zona 2
price_zone_3 |  | true | Harga menurut zona 3
price_zone_4 |  | true | Harga menurut zona 4
price_zone_5 |  | true | Harga menurut zona 5
wholesales | null | true | Harga grosir
discount | null | true | Diskon produk
taxed | null | true | Pajak produk
qty_available |  | true | Banyak produk
weight |  | true | Berat produk
is_secondhand |  | true | Pihak kedua
isbn |  | true if kind=Buku | Nomor isbn buku
with_shipping_cost |  | true | Apakah dengan biaya pengiriman
merchant_storage_id | null | false | Id Toko
is_goods |  | true | Apakah ini termasuk barang
is_umkm |  | true | Apakah termasuk usaha umkm
is_domestic |  | true | Apakah termasuk produk domestik

## Put Ubah Data Toko

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/products/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "kind": "Buku",
        "name": "Arwana Biru",
        "description": "Deskripsi Barang Buku",
        "product_category_id": "2",
        "image": "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg",
        "images": [
            "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg",
            "merchant/17/profile/ujzQ4kHZPIt4uQrLeOEfNRoL0TOxJee4AhvJPh7P.jpeg"
        ],
        "price": "10000",
        "price_zone_1": "11000",
        "price_zone_2": "12000",
        "price_zone_3": "13000",
        "price_zone_4": "14000",
        "price_zone_5": "15000",
        "wholesales": [
            {
                "quantity": 10,
                "price": 9900
            },
            {
                "quantity": 20,
                "price": 9800
            }
        ],
        "discount": "1",
        "taxed": "1",
        "qty_available": "5",
        "weight": "1500",
        "is_secondhand": "0",
        "with_shipping_cost": "1",
        "merchant_storage_id": null,
        "is_goods": "1",
        "is_umkm": "1",
        "is_domestic": "1",
        "isbn": "456165216884"
      }'
```

endpoint ini digunakan untuk merubah data produk toko,
membutuhkan isbn apabila kind = Buku.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/products/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
kind | Non Buku/Buku | true | Termasuk buku atau bukan
name |  | true | Nama barang
description |  | true | Deskripsi barang
product_category_id |  | true | Id kategori product
image |  | false | path Gambar
images |  | false | path Gambar
price |  | true | Harga Awal
price_zone_1 |  | true | Harga menurut zona 1
price_zone_2 |  | true | Harga menurut zona 2
price_zone_3 |  | true | Harga menurut zona 3
price_zone_4 |  | true | Harga menurut zona 4
price_zone_5 |  | true | Harga menurut zona 5
wholesales | null | true | Harga grosir
discount | null | true | Diskon produk
taxed | null | true | Pajak produk
qty_available |  | true | Banyak produk
weight |  | true | Berat produk
is_secondhand |  | true | Pihak kedua
isbn |  | true if kind=Buku | Nomor isbn buku
with_shipping_cost |  | true | Apakah dengan biaya pengiriman
merchant_storage_id | null | false | Id Toko
is_goods |  | true | Apakah ini termasuk barang
is_umkm |  | true | Apakah termasuk usaha umkm
is_domestic |  | true | Apakah termasuk produk domestik

## Put Ubah Status Produk Toko

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/products/{id}/status"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "negotiation_id" : "1",
      }'
```

endpoint ini digunakan untuk mengubah status produk toko.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/products/{id}/status`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | available/unavailable/archived | true | status produk

