# [Admin] Transaksi

## Get Semua Transaksi

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/orders?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "bill": "integer",
    "bill_status": "string",
    "details": {"documentDate": "datetime", "signName": "string", "signPosition": "string",…},
    "id": "integer",
    "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
    "merchant_id": "integer",
    "order_date": "datetime",
    "order_no": "string",
    "purchase_status": "string",
    "school": {"id": "string", "name": "string",…},
    "school_id": "string",
    "shipping_cost": "integer",
    "status": "string",
    "status_updated_at": "datetime",
    "tax_price": "integer",
    "total_order": "integer",
    "total_price": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/orders?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Get Detail Transaksi

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/orders/{id}/detail"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "bank_destination_id": "integer",
  "bank_mutation_in_id": "integer",
  "bank_mutation_out_id": "integer",
  "bill_status": "string",
  "compare_id": "integer",
  "courier_detail": {"name": "string", "cost": "string", "etd": "string"},
  "courier_receipt": "string",
  "courier_service_type": "string",
  "created_at": "datetime",
  "customer_order_items": [{"id": "integer", "product_id": "integer", "product_name": "string",…}],
  "details": {"documentDate": "2021-11-09 00:00:00", "signName": "string", "signPosition": "string",…},
  "funding_source": "string",
  "funding_source_ws": {"id": "string", "code": "string", "name": "string", "year": "integer"},
  "handling_fee": "integer",
  "handling_fee_details": "integer",
  "id": "integer",
  "insurance_cost": "integer",
  "invoice_file": "string",
  "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
  "merchant_id": "integer",
  "note": "string",
  "order_date": "datetime",
  "order_no": "string",
  "payments": {
    "pm1": {
      "bankAccount": "string",
      "bankDestination": "integer",
      "bankOrigin": "string",
      "date": "datetime",
      "paymentFile": "string",
      "transferred": "integer"
    }
  },
  "payment_account_no": "string",
  "payment_bank_origin": "string",
  "payment_date": "datetime",
  "payment_file": "string",
  "payment_forwarded_date": "datetime",
  "payment_method_id": "integer",
  "payment_transferred": "integer",
  "purchase_status": "string",
  "reason_cancellation": "string",
  "school": {"id": "string", "name": "string",…},
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

endpoint ini digunakan untuk mendapatkan detail data Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/orders/{id}/detail`

## Get Riwayat Transaksi

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/orders/{id}/histories"
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
    "subject_id": "string",
    "subject_type": "string",
    "updated_at": "datetime"  
  }
]
```

endpoint ini digunakan untuk mendapatkan data riwayat Transaksi.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/orders/{id}/histories`

## Get Biaya Pengiriman

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/orders/shipping-costs?q=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "bill": "integer",
    "bill_status": "string",
    "details": {"documentDate": "datetime", "signName": "string", "signPosition": "string",…},
    "id": "integer",
    "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
    "merchant_id": "integer",
    "order_date": "datetime",
    "order_no": "string",
    "purchase_status": "string",
    "school": {"id": "string", "name": "string",…},
    "school_id": "string",
    "shipping_cost": "integer",
    "status": "string",
    "status_updated_at": "datetime",
    "tax_price": "integer",
    "total_order": "integer",
    "total_price": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data biaya pengiriman jika kurir TRANSAKA.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/orders/shipping-costs?q=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
page | integer | false | Halaman

## Put Ubah Status Transaksi  

> jenis: admin

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/admin/orders/{id}/change-purchase-status"
-H 'Content-Type: application/json'
-d '{
      "purchase_status": "string"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk merubah status transaksi.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/admin/orders/{id}/change-purchase-status`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
purchase_status | string | true | Status

## Put Ubah Status Pembayaran

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/orders/{id}/change-bill-status"
-H 'Content-Type: application/json'
-d '{
      "bill_status": "string"
    }'
```
> Contoh Json Response :

```json
{
  "code": "integer",
  "message": "string"
}
```

endpoint ini digunakan untuk merubah status pembayaran.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/orders/{id}/change-bill-status`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
bill_status | string | true | Status


## Post Konfirmasi Biaya Pengiriman

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/orders/{id}/verify-shipping-cost"
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

endpoint ini digunakan untuk konfirmasi biaya pengiriman.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/orders/{id}/verify-shipping-cost`
