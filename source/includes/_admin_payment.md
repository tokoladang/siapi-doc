# [Admin] Payment

## Get Semua Pembayaran

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/payments?q=&status=&page="
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "bank_mutation_in": {"id": "integer", "admin_id": "integer",, "note": "string",…},
    "bank_mutation_in_id": "integer",
    "bank_mutation_out": {"id": "integer","admin_id": "integer", "note": "string",…},
    "bank_mutation_out_id": "integer",
    "bill": "integer",
    "bill_status": "string",
    "details": {"documentDate": "2021-06-15", "signName": "string", "signPosition": "string", "signId": "string",…},
    "handling_fee": "integer",
    "handling_fee_details": [{"name": "string", "amount": "integer"}, {"name": "string", "amount": "integer"}],
    "id": "integer",
    "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
    "merchant_id": "integer",
    "order_date": "datetime",
    "order_no": "string",
    "payment_date": "datetime",
    "payment_forwarded_date": "datetime",
    "payment_method_id": "integer",
    "payment_transferred": "integer",
    "payments": {"pm2": {"va": "string", "amount": "integer", "expired": "datetime", "paid": "boolean",…}},
    "school": {"id": "string", "name": "string",…},
    "school_id": "string",
    "shipping_cost": "integer",
    "status_updated_at": "datetime",
    "tax_price": "integer",
    "total_order": "integer",
    "total_price": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data pembayaran.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/payments?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | Kata kunci
status | string | false | Status
page | integer | false | Halaman

## Get Ringkasan Pembayaran

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/payments/summary"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
  "forwarded": "integer",
  "paid": "integer",
  "unpaid": "integer"
}
```

endpoint ini digunakan untuk mendapatkan data ringkasan pembayaran.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/payments/summary`

## Get Pembayaran By Penjual

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/payments/{merchant}/merchant?q&status&page"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
    "bank_mutation_in": {"id": "integer", "admin_id": "integer",, "note": "string",…},
    "bank_mutation_in_id": "integer",
    "bank_mutation_out": {"id": "integer","admin_id": "integer", "note": "string",…},
    "bank_mutation_out_id": "integer",
    "bill": "integer",
    "bill_status": "string",
    "details": {"documentDate": "2021-06-15", "signName": "string", "signPosition": "string", "signId": "string",…},
    "handling_fee": "integer",
    "handling_fee_details": [{"name": "string", "amount": "integer"}, {"name": "string", "amount": "integer"}],
    "id": "integer",
    "merchant": {"id": "integer", "name": "string", "email": "string", "phone": "string",…},
    "merchant_id": "integer",
    "order_date": "datetime",
    "order_no": "string",
    "payment_date": "datetime",
    "payment_forwarded_date": "datetime",
    "payment_method_id": "integer",
    "payment_transferred": "integer",
    "payments": {"pm2": {"va": "string", "amount": "integer", "expired": "datetime", "paid": "boolean",…}},
    "school": {"id": "string", "name": "string",…},
    "school_id": "string",
    "shipping_cost": "integer",
    "status_updated_at": "datetime",
    "tax_price": "integer",
    "total_order": "integer",
    "total_price": "integer"
  }
]
```

endpoint ini digunakan untuk mendapatkan data Payment berdasarkan penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/payments/{merchant}/merchant?q&status&page`

## Post verifikasi Pembayaran

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{orderId}/verify"
-H 'Content-Type: application/json'
-d '{
      "system_bank_id": "integer",
      "client_bank": {
          "bank": "string",
          "name": "string",
          "no": "string"
      },
      "transferred": "integer",
      "transferred_at": "datetime",
      "note": "string",
      "bank_mutation_id": "integer",
      "is_valid": "boolean"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "message"
}
```

endpoint ini digunakan untuk verifikasi pembayaran.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{orderId}/verify`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
system_bank_id | integer | true | sistem bank
client_bank.bank | string | true | bank
client_bank.name | string | true | nama bank
client_bank.no | string | true | no. bank
transferred | integer | true | status transfer
transferred_at | datetime | true | tanggal transfer
note | string | false | catatan
bank_mutation_id | integer | false | mutasi bank
is_valid | boolean | true | valid

## Post verifikasi ulang pesanan

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{orderId}/reverify"
-H 'Content-Type: application/json'
-d '{
      "system_bank_id": "integer",
      "client_bank": {
          "bank": "string",
          "name": "string",
          "no": "string"
      },
      "transferred": "integer",
      "transferred_at": "datetime",
      "note": "string",
      "bank_mutation_id": "integer",
      "is_valid": "boolean"
    }'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "message"
}
```

endpoint ini digunakan untuk verifikasi ulang pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{orderId}/reverify`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
system_bank_id | integer | true | sistem bank
client_bank.bank | string | true | bank
client_bank.name | string | true | nama bank
client_bank.no | string | true | no. bank
transferred | integer | true | status transfer
transferred_at | datetime | true | tanggal transfer
note | string | false | catatan
bank_mutation_id | integer | false | mutasi bank
is_valid | boolean | true | valid

## Post Biaya Admin

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{orderId}/handling-fees"
-H 'Content-Type: application/json'
-d '{
    "free": "boolean",
    "fees": {
        "name": "string",
        "amount": "integer"
    }
}'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk verifikasi biaya penanganan pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{orderId}/handling-fees`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
free | boolean | true | status biaya pengiriman
fees.name | string | true if free false | nama pengiriman
fees.amount | integer | true if free false | biaya pengiriman

## Post pesanan forwarded

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{merchantId}/forward"
-H 'Content-Type: application/json'
-d '{
    "orders": {
        "id": "integer"
    }, 
    "note": "string",
    "system_bank_id": "integer", 
    "transferred_at": "datetime"
}'
```
> Contoh Json Response :

```json
{
    "code": "integer",
    "message": "string"
}
```

endpoint ini digunakan untuk verifikasi biaya penanganan pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{merchantId}/forward`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
orders.id | integer | true | pesanan
note | string | false | catatan
system_bank_id | integer | true | sistem bank
transferred_at | date | true | tanggal
