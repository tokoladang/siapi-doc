# [Admin] Toko

## Kategori Produk
### Get Kategori Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/product-categories"
-H 'Content-Type: application/json'
-d '{}'
```

endpoint ini digunakan untuk mendapatkan data kategori produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/product-categories`

### Simpan Kategori Produk

> jenis: public

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

### Ubah Kategori Produk

> jenis: public

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

### Hapus Kategori Produk

> jenis: public

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}"
-H 'Content-Type: application/json'
-d '{}'
```

endpoint ini digunakan untuk menghapus kategori produk.

### HTTP Request

`DELETE https://staging.siapi.tokoladang.co.id/admin/product-categories/{id}`

## Produk

### Get Produk

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products?q=&status="
-H 'Content-Type: application/json'
-d '{}'
```

endpoint ini digunakan untuk mendapatkan data produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products?q=&status=`

### Get Produk berdasarkan id

> jenis: public

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products/{id}"
-H 'Content-Type: application/json'
-d '{}'
```

endpoint ini digunakan untuk mendapatkan data produk berdasarkan id.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products/{id}`

### Update status produk

> jenis: public

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/products/{id}/status"
-H 'Content-Type: application/json'
-d '{
    "status": "update_status"
}'
```

endpoint ini digunakan untuk mengubah status produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/products/{id}/status`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | null | true | Status produk