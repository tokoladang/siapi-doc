# [Buyer] Perbandingan

## Menambahkan perbandingan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/compares/new"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "code": "Perbandingan Baru",
}'
```

endpoint ini digunakan untuk menambahkan perbandingan barang.

`POST https://staging.siapi.tokoladang.co.id/buyer/compares/new`

### Query Body

| Parameter | Default | required | Deskripsi |
| --------- | ------- | -------- | --------- |
| code      | null    | true     |           |

## Update data perbandingan

> jenis: buyer

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/buyer/compares/101/update"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "code": "Update Perbandingan Baru",
}'
```

endpoint ini digunakan untuk update data perbandingan barang.

`PUT https://staging.siapi.tokoladang.co.id/buyer/compares/{$compare->id}/update`

### Query Body

| Parameter | Default | required | Deskripsi |
| --------- | ------- | -------- | --------- |
| code      | null    | true     |           |

## Menghapus Perbandingan

> jenis: buyer

```shell
curl -X DELETE "https://staging.siapi.tokoladang.co.id/buyer/compares/101/remove"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{

}'
```

endpoint ini digunakan untuk menghapus perbandingan barang.

`DELETE https://staging.siapi.tokoladang.co.id/buyer/compares/{$compare->id}/update`
