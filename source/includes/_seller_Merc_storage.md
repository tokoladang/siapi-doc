# [Seller] Merchant Storage

Merchant Storage digunakan untuk mengambil data etalase toko, membuat data etalase, merubah data etalase, dan menghapus etalase.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## Get Semua data Etalase 

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/merchant-storages"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
{
  "id": 1,
  "merchant_id": 92,
  "name": "Buku Gambar",
},
{
  "id": 2,
  "merchant_id": 92,
  "name": "Buku Menulis",
}
```

endpoint ini digunakan untuk mendapatkan data etalase.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/merchant-storages`


## Post Tambah data Etalase

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/merchant-storages"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "Buku Gambar",
      }'
```

endpoint ini digunakan untuk membuat data etalase sesuai toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/merchant-storages`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | null | true | Nama Etalase

## Put Ubah data etalase

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/merchant-storages/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "Buku Menulis",
      }'
```

endpoint ini digunakan untuk mengubah data nama etalase toko.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/merchant-storages/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | null | true | Nama Etalase


## Delete Hapus data Etalase

> jenis: seller

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/merchant-storages/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
```

endpoint ini digunakan untuk menghapus data etalase toko.

### HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/seller/merchant-storages/{id}`
