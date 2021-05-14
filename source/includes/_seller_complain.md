# [Seller] Complain

## Get Semua Komplain Penjual

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/complains"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
    {
        "id": "",
        "merchant_id": "",
        "customer_id": "",
        "code": "",
        "message": "",
        "status": "",
        "customer_order_id": "",
        "school_id": "",
        "created_by": "",
        "updated_by": "",
        "created_at": "",
        "updated_at": "",
        "merchant": {...},
        "customer": {...},
        "customer_order": {...}
    },
    {...}
]
```

endpoint ini digunakan untuk mendapatkan data Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/complains`

## Get Komplain Detail Penjual

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/complains/{complain}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "id":"",
    "merchant_id":"",
    "customer_id":"",
    "code":"",
    "message":"",
    "status":"",
    "customer_order_id":"",
    "school_id":"",
    "updated_at":"",
    "merchant": {...},
    "customer": {...},
    "customer_order": {...},
    "merchant_complain_history": [{...}, {...}]
}
```

endpoint ini digunakan untuk mendapatkan data detail Komplain.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/complains/{complain}`

## POST penjual tanggapi Komplain

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/complains/{complain}"
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

`POST https://staging.siapi.tokoladang.co.id/seller/complains/{complain}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | null | true | Pesan

## PUT Penjual ubah status komplain

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/complains/{complain}"
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

`PUT https://staging.siapi.tokoladang.co.id/seller/complains/{complain}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | null | true | Pesan