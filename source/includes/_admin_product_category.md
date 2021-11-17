# [Admin]Kategori Produk

## Get semua Kategori Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/product-categories?parent="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "created_by": "string",
    "description": "string",
    "enabled": "true",
    "id": "integer",
    "image": "string",
    "level": "integer",
    "name": "string",
    "parent_id": "integer",
    "sequence": "integer",
    "slug": "string",
    "updated_at": "datetime",
    "updated_by": "string",
    "_lft": "integer",
    "_rgt": "integer",
  }
]
```

endpoint ini digunakan untuk mendapatkan data kategori produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/product-categories?parent=`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
parent | string | false | id parent kategori

## Simpan Kategori Produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/product-categories"
-H 'Content-Type: application/json'
-d '{    
      "name": "string",
      "sequence": "integer",
      "image": "file",
      "enabled": "boolean"
    }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menyimpan kategori produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/product-categories`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Kategori
sequence | integer | true | Sequence
image | file | false | Gambar ikon
enabled | boolean | true | Status kategori

## Ubah Kategori Produk

> jenis: admin

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}"
-H 'Content-Type: application/json'
-d '{    
      "name": "string",
      "sequence": "integer",
      "image": "file",
      "enabled": "boolean"
    }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk mengubah kategori produk.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Kategori
sequence | integer | true | Sequence
image | file | false | Gambar ikon
enabled | boolean | true | Status kategori

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
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menghapus kategori produk.

### HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`
