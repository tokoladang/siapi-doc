# [Seller] Transaksi

Transaksi digunakan untuk mengambil data riwayat Pembelian toko, merubah status dari Proses pesanan, menolah pesanan dan mengirim pesanan.

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## DATA Transaksi

## Get Semua Data Transaksi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/orders?q=&status=&page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```

> Contoh Json Response :

```json
{
  "current_page": "integer",
  "data": [
    {
      "bank_destination_id": "integer",
      "bank_mutation_in": "integer",
      "bank_mutation_in_id": "integer",
      "bank_mutation_out_id": "integer",
      "bill_status": "string",
      "compare_id": "integer",
      "courier_detail": "json",
      "courier_receipt": "string",
      "courier_service_type": "string",
      "created_at": "datetime",
      "details": {
        "documentDate": "date",
        "lateCharge": "integer",
        "lateChargeNote": "string",
        "signId": "string",
        "signName": "string",
        "signPhone": "string",
        "signPosition": "string",
        "taxPrice": "integer",
        "totalPrice": "integer",
        "totalQty": "integer"
      },
      "funding_source": "string",
      "funding_source_ws": "json",
      "handling_fee": "integer",
      "handling_fee_details": [{"name": "string", "amount": "integer"}, {"name": "string", "amount": "integer"}],
      "id": "integer",
      "insurance_cost": "integer",
      "invoice_file": "string",
      "merchant_id": "integer",
      "note": "string",
      "order_date": "datetime",
      "order_no": "string",
      "payment_account_no": "string",
      "payment_bank_origin": "string",
      "payment_date": "datetime",
      "payment_file": "string",
      "payment_forwarded_date": "datetime",
      "payment_method_id": "integer",
      "payment_transferred": "integer",
      "payments": {
        "pm" : {
          "bankAccount": "integer",
          "bankDestination": "integer",
          "bankOrigin": "string",
          "date": "datetime",
          "paymentFile": "string",
          "transferred": "integer"
        }
      },
      "purchase_status": "string",
      "reason_cancellation": "string",
      "school": {"id": "string", "name": "string", "image": null, "details": "json",…},
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
  ],
  "first_page_url": "string",
  "from": "integer",
  "last_page": "integer",
  "last_page_url": "string",
  "links": [],
  "next_page_url": "string",
  "path": "string",
  "per_page": "integer",
  "prev_page_url": "string",
  "to": "integer",
  "total": "integer"
}
```
endpoint ini digunakan untuk mendapatkan data Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/orders?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci pencarian
status | string | false | Kata kunci status
page | string | false | Halaman

## Get Data Detail Transaksi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/orders/{id}"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```

> Contoh Json Response :

```json
{
  "bank_destination_id": "integer",
  "bank_mutation_in": "integer",
  "bank_mutation_in_id": "integer",
  "bank_mutation_out_id": "integer",
  "bill_status": "string",
  "compare_id": "integer",
  "courier_detail": "json",
  "courier_receipt": "string",
  "courier_service_type": "string",
  "created_at": "datetime",
  "details": {
    "documentDate": "date",
    "lateCharge": "integer",
    "lateChargeNote": "string",
    "signId": "string",
    "signName": "string",
    "signPhone": "string",
    "signPosition": "string",
    "taxPrice": "integer",
    "totalPrice": "integer",
    "totalQty": "integer"
  },
  "funding_source": "string",
  "funding_source_ws": "json",
  "handling_fee": "integer",
  "handling_fee_details": [{"name": "string", "amount": "integer"}, {"name": "string", "amount": "integer"}],
  "id": "integer",
  "insurance_cost": "integer",
  "invoice_file": "string",
  "merchant_id": "integer",
  "note": "string",
  "order_date": "datetime",
  "order_no": "string",
  "payment_account_no": "string",
  "payment_bank_origin": "string",
  "payment_date": "datetime",
  "payment_file": "string",
  "payment_forwarded_date": "datetime",
  "payment_method_id": "integer",
  "payment_transferred": "integer",
  "payments": {
    "pm" : {
      "bankAccount": "integer",
      "bankDestination": "integer",
      "bankOrigin": "string",
      "date": "datetime",
      "paymentFile": "string",
      "transferred": "integer"
    }
  },
  "purchase_status": "string",
  "reason_cancellation": "string",
  "school": {"id": "string", "name": "string", "image": null, "details": "json",…},
  "school_id": "string",
  "shipping_cost": "integer",
  "status_updated_at": "datetime",
  "tax_payer": "string",
  "tax_price": "integer",
  "time_limit": "integer",
  "total_price": "integer",
  "total_qty": "integer",
  "total_weight": "integer",
  "updated_at": "datetime",
  "customer_order_items": [
    {
      "bast": {"quantity": "integer", "totalPrice": "integer", "taxPrice": "integer"},
      "quantity": "integer",
      "taxPrice": "integer",
      "totalPrice": "integer",
      "created_at": "datetime",
      "created_by": "string",
      "customer_order_id": "integer",
      "id": "integer",
      "item_no": "integer",
      "negotiation": {"id": "integer", "status_nego": "string"},
      "negotiation_id": "integer",
      "price": "integer",
      "product_id": "integer",
      "product_image": "string",
      "product_name": "string",
      "quantity": "integer",
      "shipping": "json",
      "tax_price": "integer",
      "total_price": "integer",
      "updated_at": "datetime",
      "updated_by": "string"
    }
  ]
}
```
endpoint ini digunakan untuk mendapatkan data detail Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/orders/{id}`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci pencarian
status | string | false | Kata kunci status
page | string | false | Halaman



## Post Pembatalan Transaksi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process-canceling"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "status" : "string"
      }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk memproses pembatalan Transaksi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process-canceling`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | string | true | terima / tolak

## Post Perubahan Transaksi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process-updating"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "status" : "string"
      }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk memproses perubahan Transaksi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process-updating`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | string | true | terima / tolak

## Post Proses Transaksi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "time_limit" : "integer",
        "shipping_cost" : "integer",
        "shipping_etd" : "integer"
      }'
```

> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk memproses Transaksi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/process`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
time_limit | integer | true | Lama estimasi pengerjaan
shipping_cost |integer  | false | Ongkos pengerjaan
shipping_etd | integer | false | Estimasi pengiriman

## Post Tolak Transaksi

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/reject"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menolak Transaksi dari pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/reject`

## Post Kirim Pemesanan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/send"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "courier_receipt": "string"
      }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk menyetujui dan mengirim Transaksi pembeli.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/send`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
courier_receipt | string | false | No. Resi Transaksi

## Post Pickup Pemesanan

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/pickup"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk pickup Transaksi pembeli jika menggunakan kurir TRANSAKA.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/orders/{id}/pickup`

## Get Log aktifitas Transaksi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/orders/{id}/log"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```
> Contoh Json Response :

```json
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
```

endpoint ini digunakan untuk mendapatkan aktifitas Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/orders/{id}/log`

## Get Ekspor Data Transaksi

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/orders/document/export"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{}'
```
> Contoh Json Response :

```json
"File Excel"
```

endpoint ini digunakan untuk ekspor data Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/orders/document/export`
