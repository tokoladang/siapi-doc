# [Seller] Etalase 

Etalase digunakan untuk mengelompokan Produk.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## DATA Etalase Toko

## Get Semua data Etalase 

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/merchant-storages"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
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

endpoint ini digunakan untuk mendapatkan data etalase.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/merchant-storages`

## Post Tambah Etalase Baru

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/merchant-storages"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "string"
      }'
```

endpoint ini digunakan untuk membuat data etalase baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/merchant-storages`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Etalase

## Put Ubah Data Etalase

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/merchant-storages/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "string"
      }'
```

endpoint ini digunakan untuk mengubah data nama etalase toko.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/merchant-storages/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Etalase


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
