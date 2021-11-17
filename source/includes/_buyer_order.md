# [Buyer] Transaksi

<aside class="notice">
  membutuhkan Autentikasi/Token <strong>buyer</strong>.
</aside>

## Get Data Transaksi

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/orders?q=&status=&page="
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```
> Contoh Json Response :

```json
[
  {
    "bank_destination_id": "integer",
    "bank_mutation_in_id": "integer",
    "bank_mutation_out_id": "integer",
    "bill_status": "unpaid",
    "cant_apply": "boolean",
    "compare_id": "integer",
    "courier_detail": {"name": "string", "etd": "string", "cost": "integer", "address": "string"},
    "courier_receipt": "string",
    "courier_service_type": "string",
    "created_at": "datetime",
    "customer_order_items": [
      {
        "id": "integer", "product_id": "integer", "quantity": 1, "price": "integer", "total_price": "integer", "bast": "json", 
        "customer_order_id": "integer", "item_no": "integer", "negotiation_id": "integer",  "product_image": "string",
        "product_name": "string", "tax_price": "integer", "shipping": {
          "quantity": "integer", "weight": "integer", "length": "integer", "width": "integer", "height": "integer"
        }
      }
    ],
    "details": "json",
    "funding_source": "string",
    "funding_source_ws": {"id": "string", "code": "string", "name": "string", "year": "integer"},
    "handling_fee": "integer",
    "handling_fee_details": "json",
    "id": "integer",
    "insurance_cost": "integer",
    "invoice_file": "string",
    "merchant": {"id": "integer", "name": "string", "image": "string"},
    "merchant_id": "integer",
    "note": "string",
    "order_date": "datetime",
    "order_no": "string",
    "over_time_limit": "integer",
    "payment_account_no": "string",
    "payment_bank_origin": "string",
    "payment_date": "datetime",
    "payment_file": "string",
    "payment_forwarded_date": "datetime",
    "payment_method_id": "integer",
    "payment_transferred": "integer",
    "payments": "json",
    "purchase_status": "string",
    "reason_cancellation": "string",
    "school_id": "string",
    "shipping_cost": "integer",
    "status_updated_at": "datetime",
    "tax_payer": "string",
    "tax_price": "integer",
    "time_limit": "integer",
    "total_price": "integer",
    "total_qty": "integer",
    "total_weight": "integer",
    "updated_at": "datetime"
  }
]
```
endpoint ini digunakan untuk mendapatkan data transaksi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/orders?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Get Detail Data Transaksi

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/detail"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```
> Contoh Json Response :

```json
{
  "bank_destination_id": "integer",
  "bank_mutation_in_id": "integer",
  "bank_mutation_out_id": "integer",
  "bill_status": "unpaid",
  "cant_apply": "boolean",
  "compare_id": "integer",
  "courier_detail": {"name": "string", "etd": "string", "cost": "integer", "address": "string"},
  "courier_receipt": "string",
  "courier_service_type": "string",
  "created_at": "datetime",
  "customer_order_items": [
    {
      "id": "integer", "product_id": "integer", "quantity": 1, "price": "integer", "total_price": "integer", "bast": "json", 
      "customer_order_id": "integer", "item_no": "integer", "negotiation_id": "integer",  "product_image": "string",
      "product_name": "string", "tax_price": "integer", "shipping": {
        "quantity": "integer", "weight": "integer", "length": "integer", "width": "integer", "height": "integer"
      }
    }
  ],
  "details": "json",
  "funding_source": "string",
  "funding_source_ws": {"id": "string", "code": "string", "name": "string", "year": "integer"},
  "handling_fee": "integer",
  "handling_fee_details": "json",
  "id": "integer",
  "insurance_cost": "integer",
  "invoice_file": "string",
  "merchant": {"id": "integer", "name": "string", "image": "string"},
  "merchant_id": "integer",
  "note": "string",
  "order_date": "datetime",
  "order_no": "string",
  "over_time_limit": "integer",
  "payment_account_no": "string",
  "payment_bank_origin": "string",
  "payment_date": "datetime",
  "payment_file": "string",
  "payment_forwarded_date": "datetime",
  "payment_method_id": "integer",
  "payment_transferred": "integer",
  "payments": "json",
  "purchase_status": "string",
  "reason_cancellation": "string",
  "school_id": "string",
  "shipping_cost": "integer",
  "status_updated_at": "datetime",
  "tax_payer": "string",
  "tax_price": "integer",
  "time_limit": "integer",
  "total_price": "integer",
  "total_qty": "integer",
  "total_weight": "integer",
  "updated_at": "datetime"
}
```
endpoint ini digunakan untuk mendapatkan detail transaksi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/detail`

## Get Riwayat Data Transaksi

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/activities"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```
> Contoh Json Response :

```json
[
  {
    "causer_id": "string",
    "causer_type": "string",
    "created_at": "datetime",
    "description": "string",
    "event": "string",
    "id": "integer",
    "log_name": "string",
    "properties": {"user": {"id": "integer", "email": "string", "name": "string"},…},
    "subject_id": "181",
    "subject_type": "App\\Models\\CustomerOrder",
    "updated_at": "datetime"
  }
]
```
endpoint ini digunakan untuk mendapatkan riwayat detail transaksi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/activities`

## Post Proses Transaksi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/process"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "status": "string"
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk memproses transaksi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/process`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
status | string | true | Status transaksi

## Post Pembatalan Transaksi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/canceling"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk membatalkan transaksi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/canceling`

## Post Perubahan Transaksi

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/updating"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "items": [
          {"id": "integer", "qty": "integer"}
        ]
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk pengajuan perubahan transaksi.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/updating`

### Query Body

Parameter  | Default | required | Deskripsi    
---------- | ------- | -------- | -------------
items.*.id | integer | true | Id Produk
items.*.qty | integer | true | Jumlah

## Post Setuju Penawaran Penjual

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{{id}}/process-merchant-offer"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "accept": "boolean",
}'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk menerima tawaran batas waktu yang di ajukan penjual.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/process-merchant-offer`

### Query Body

| Parameter | Default | required | Deskripsi          |
| --------- | ------- | -------- | ------------------ |
| accept    | boolean | true     | true / false

## Get Lacak Transaksi

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/tracking"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
  "cn_no": "string",
  "location": "string",
  "process_latitude": "string",
  "process_longitude": "string",
  "process_maps_location": "string",
  "process_photo": "string",
  "process_received_by": "string",
  "process_received_relation": "string",
  "process_signature": "string",
  "status": "string",
  "status_stage": "string",
  "time": "datetime"
}
```

endpoint ini digunakan untuk melacak transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/tracking`

## Post Terima pesanan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/receive"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk menerima pesanan.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/receive`

## Post Atur BAST

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/bast"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "bast": {
            "document_date": "date",
            "sign_name": "string",
            "sign_position": "string",
            "sign_id": "string",
            "sign_phone": "string",
            "late_charge": "integer",
            "late_charge_note": "string",
            "images"; []
        },
        "bastItems": [
          {"id": "integer", "quantity": "integer"}
        ]
      }'
```

> Contoh Json Response:

```json
{
   "code": "integer",
   "message": "string"
}
```

endpoint ini digunakan untuk mengatur BAST.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/bast`

### Query Body

Parameter      | Default | required | Deskripsi                   
-------------- | ------- | -------- | --------------------------- 
bast.*.document_date | string | true | Tanggal Dokumen             
bast.*.sign_name | string | true | Nama Penerima BAST          
bast.*.sign_position | string | true | Jabatan Penerima BAST       
bast.*.sign_id | string | false | NIP/NIPY Penerima BAST      
bast.*.sign_phone | string | false | Telepon Penerima BAST       
bast.*.late_charge | integer | false | Denda Keterlambatan         
bast.*.late_charge_note | string | false | Catatan Denda Keterlambatan 
bast.*.images | array | false | Bukti gambar 
bast_items.*.id | integer | true | Id item           
bast_items.*.quantity | integer | true | Jumlah item           

## Post Pembayaran Manual / Transfer

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment1"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "date": "datetime",
        "bank_origin": "string",
        "bank_account": "string",
        "bank_destination": "integer",
        "transferred": "integer",
        "payment_file":"string"
      }'
```

endpoint ini digunakan untuk mengatur pembayaran secara manual / transfer.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment1`

### Query Body

| Parameter       | Default | required | Deskripsi
| --------------- | ------- | -------- | -----------------
| date | date | true | Tanggal Pembayaran
| bank_origin | string | true | Nama Bank         
| bank_account | string | true | Akun Bank         
| bank_destination | integer | true | Bank Tujuan       
| transferred | integer | true | Jumlah yang ditransfer
| payment_file | string | true | Bukti Pembayaran  

## Post Generate Pembayaran BRIVA

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/create-va2"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
  "pm2": {
    "amount": "integer",
    "expired": "datetime",
    "paid": "boolean",
    "va": "string"
  }
}
```

endpoint ini digunakan untuk generate pembayaran melalui BRI Virtual Account.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/create-va2`

## Post Pembayaran BRIVA

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment2"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "date": "date",
        "payment_file": "file|image"
      }'
```

> Contoh Json Response

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk mengatur pembayaran melalui BRIVA.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment2`

### Query Body

Parameter      | Default | required | Deskripsi                   
-------------- | ------- | -------- | --------------------------- 
date | date | true | Tanggal             
payment_file | file | true | Gambar

## Post Generate Pembayaran BPD

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/create-va3"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{}
```

endpoint ini digunakan untuk generate pembayaran melului BPD.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/create-va3`

## Post Pembayaran BPD

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment3"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "date": "date",
        "payment_file": "file|image"
      }'
```

> Contoh Json Response

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk mengatur pembayaran melalui BPD.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment3`

### Query Body

Parameter      | Default | required | Deskripsi                   
-------------- | ------- | -------- | --------------------------- 
date | date | true | Tanggal             
payment_file | file | true | Gambar

## Post Generate Pembayaran Bank Jatim

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/create-va4"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
  "pm4": {
    "amount": "integer",
    "expired": "date",
    "paid": "boolean",
    "va": "string"
  }
}
```

endpoint ini digunakan untuk generate pembayaran melului Bank Jatim.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/create-va4`

## Post Pembayaran Bank Jatim

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment4"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "date": "date",
        "payment_file": "file|image"
      }'
```

> Contoh Json Response

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk mengatur pembayaran melalui Bank Jatim.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{id}/payment4`

### Query Body

Parameter      | Default | required | Deskripsi                   
-------------- | ------- | -------- | --------------------------- 
date | date | true | Tanggal             
payment_file | file | true | Gambar

## Get Review Toko

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/orders/{orderId}/merchant-review"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
  "created_at": "datetime",
  "customer_order_id": "integer",
  "id": "integer",
  "message": "string",
  "rating": "integer",
  "merchant_id": "integer",
  "school_id": "string",
  "updated_at": "datetime"
}
```

endpoint ini digunakan untuk mendapatkan review toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/orders/{orderId}/merchant-review`

## Get Review Produk

> jenis: buyer

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/buyer/orders/{orderItemId}/product-review"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> Contoh Json Response:

```json
{
  "created_at": "datetime",
  "customer_order_item_id": "integer",
  "id": "integer",
  "message": "string",
  "product_id": "string",
  "rating": "integer",
  "school_id": "string",
  "updated_at": "datetime"
}
```

endpoint ini digunakan untuk mendapatkan review produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/buyer/orders/{orderItemId}/product-review`

## Post Komentar Review Toko

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{orderId}/merchant-review"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "rating": "integer",
        "message": "string"
      }'
```

> Contoh Json Response

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk memberi review terhadap toko.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{orderId}/merchant-review`

### Query Body

Parameter      | Default | required | Deskripsi                   
-------------- | ------- | -------- | --------------------------- 
rating | integer | true | Penilaian             
message | string | true | Komentar

## Post Komentar Review Produk

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/{orderItemId}/product-review"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
        "rating": "integer",
        "message": "string"
      }'
```

> Contoh Json Response

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk memberi review terhadap toko.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{orderItemId}/product-review`

### Query Body

Parameter      | Default | required | Deskripsi                   
-------------- | ------- | -------- | --------------------------- 
rating | integer | true | Penilaian             
message | string | true | Komentar
