# [Admin] Complain

## Get Semua Komplain Admin

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/complains"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
    {
        "id": 1,
        "merchant_id": 92,
        "customer_id": 1,
        "code": "5FEAABAB83B81",
        "message": "komplain 1",
        "status": "done",
        "customer_order_id": 1,
        "school_id": "4BB64007-F3F0-3C97-AF26-4FF94EBC52C4",
        "updated_at": "2021-01-02T08:15:29.000000Z",
        "merchant": {...},
        "customer": {...},
        "customer_order": {...},

    },
    {....}
]
```

endpoint ini digunakan untuk mendapatkan data Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/complains`

## Get Komplain detail Admin

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/complains/{complain}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "id": 1,
    "merchant_id": 92,
    "customer_id": 1,
    "code": "5FEAABAB83B81",
    "message": "komplain 1",
    "status": "done",
    "customer_order_id": 1,
    "school_id": "4BB64007-F3F0-3C97-AF26-4FF94EBC52C4",
    "updated_at": "2021-01-02T08:15:29.000000Z",
    "merchant": {...},
    "customer": {...},
    "customer_order": {...},
    "merchant_complain_history": [{...}, {...}]

}
```

endpoint ini digunakan untuk mendapatkan data Komplain berdasarkan ID.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/complains/{complain}`

## POST Admin tanggapi Komplain

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/complains/{complain}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Berhasil menyimpan data"
}
```

endpoint ini digunakan untuk menambah pesan pada komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/complains/{complain}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | null | true | Pesan

## PUT Admin ubah status komplain

> jenis: admin

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/admin/complains/{complain}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Berhasil menyimpan data"
}
```

endpoint ini digunakan untuk mengubah status komplain.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/admin/complains/{complain}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | null | true | Pesan