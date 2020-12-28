# [Admin]Kategori Produk

## Get semua Kategori Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/product-categories"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk mendapatkan data kategori produk.

## HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/product-categories`

## Simpan Kategori Produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/product-categories"
-H 'Content-Type: application/json'
-d '{    
    "name": "Kategori"
    "sequence": ""
    "description": "Kategori Baru"
    "image": ""
    "enabled": "true"
}'
```

> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk menyimpan kategori produk.

## HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/product-categories`

## Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | null | true | Nama Kategori
sequence | null | true | Sequence
description | null | true | Deskripsi
image | null | image | Gambar ikon
enabled | null | true | Status kategori

## Ubah Kategori Produk

> jenis: admin

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}"
-H 'Content-Type: application/json'
-d '{
    "name": "Kategori"
    "sequence": ""
    "description": "Kategori Baru"
    "image": ""
    "enabled": "true"
}'
```

> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk mengubah kategori produk.

## HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`

## Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | null | true | Nama Kategori
sequence | null | true | Sequence
description | null | true | Deskripsi
image | null | image | Gambar ikon
enabled | null | true | Status kategori

## Hapus Kategori Produk

> jenis: admin

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}"
-H 'Content-Type: application/json'
-d '{}'
```

> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk menghapus kategori produk.

## HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`