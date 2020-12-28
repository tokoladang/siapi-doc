# [Admin]Produk

## Get semua Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products?q=&status="
-H 'Content-Type: application/json'
-d '{}'
```

Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk mendapatkan data produk.

## HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products?q=&status=`

## Get salah satu Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products/{id}"
-H 'Content-Type: application/json'
-d '{}'
```

Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk mendapatkan data produk berdasarkan id.

## HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products/{id}`

## Update status produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/products/{id}/status"
-H 'Content-Type: application/json'
-d '{
    "status": "update_status"
}'
```

Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk mengubah status produk.

## HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/products/{id}/status`

## Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | null | true | Status produk