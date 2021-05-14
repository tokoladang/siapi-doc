# [Buyer] Complain

## Get Semua Komplain Pembeli

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/complains"
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

`GET https://staging.siapi.tokoladang.co.id/buyer/complains`

## Get Komplain detail Pembeli

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/complains/{complain}"
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

`GET https://staging.siapi.tokoladang.co.id/buyer/complains/{complain}`

## POST Pembeli Komplain baru.

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/complains"
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

endpoint ini digunakan untuk komplain baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/complains`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
customer_order_id | null | true | id pesanan
code | null | true | Kode
merchant_id | null | true | id Toko
message | null | true | Pesan

## POST Pembeli tanggapi Komplain.

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/complains/{complain}"
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

endpoint ini digunakan untuk menanggapi pesan pada komplain.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/complains/{complain}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | null | true | Pesan

## PUT Pembeli ubah status komplain

> jenis: buyer

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

`PUT https://staging.siapi.tokoladang.co.id/buyer/complains/{complain}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
message | null | true | Pesan