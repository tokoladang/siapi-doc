# [Seller] Order

Order digunakan untuk mengambil data riwayat Pembelian toko, merubah status dari Proses pesanan, menolah pesanan dan mengirim pesanan.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

<!-- ### GET Data

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

`GET https://staging.siapi.tokoladang.co.id/seller/products` -->

## Post Ubah Status (Proses) Pemesanan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "time_limit" : 10,
        "shipping_cost" : 50000,
        "shipping_etd" : 7
      }'
```

> Contoh Json Response :

```json
{
    "message": "Order Berhasil di proses dan Menunggu Respon Pembeli."
}
```

endpoint ini digunakan untuk memproses pesanan dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
time_limit |  | true | Lama estimasi pengerjaan
shipping_cost |  | false | Ongkos pengerjaan
shipping_etd |  | false | Estimasi pengiriman

## Post Ubah Status (Tolak) Pemesanan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/reject"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
```
> Contoh Json Response :

```json
{
    "message": "Order Berhasil ditolak."
}
```

endpoint ini digunakan untuk menolak pesanan dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/reject`


## Post Ubah Status (Kirim) Pemesanan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/send"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
```
> Contoh Json Response :

```json
{
    "message": "Status Order Berhasil diubah menjadi dikirim."
}
```

endpoint ini digunakan untuk menyetujui dan mengirim pesanan pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/send`
