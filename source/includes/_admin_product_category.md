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
[
  {
        "id": 1,
        "name": "Tempore est nesciunt laudantium consequuntur beatae vero est eum.",
        "parent_id": null,
        "sequence": 1,
        "description": "Recusandae quis aspernatur ea quis fuga.",
        "enabled": true,
        "image": "https://lorempixel.com/100/100/food",
        "level": 2,
        "slug": "tempore-est-nesciunt-laudantium-consequuntur-beatae-vero-est-eum",
        "created_by": null,
        "updated_by": null,
        "created_at": "2020-12-29T04:08:10.000000Z",
        "updated_at": "2020-12-29T04:08:10.000000Z"
    },
    {...}
]
```

endpoint ini digunakan untuk mendapatkan data kategori produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/product-categories`

## Simpan Kategori Produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/product-categories"
-H 'Content-Type: application/json'
-d '{    
    "name": "Pelengkap"
    "sequence": "1"
    "description": "deskripsi"
    "image": ""
    "enabled": "true"
}'
```

> Contoh Json Response :

```json
{
  "code": 200,
  "message": "Kategori Produk Berhasil disimpan"
}
```

endpoint ini digunakan untuk menyimpan kategori produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/product-categories`

### Query Body

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
    "name": "Pelengkap 2"
    "sequence": "1"
    "description": "deskripsi"
    "image": ""
    "enabled": "true"
}'
```

> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Kategori Produk Berhasil disimpan"
}
```

endpoint ini digunakan untuk mengubah kategori produk.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`

### Query Body

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
    "code": 200,
    "message": "Kategori Produk Berhasil dihapus"
}
```

endpoint ini digunakan untuk menghapus kategori produk.

### HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`