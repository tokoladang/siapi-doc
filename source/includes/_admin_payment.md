# [Admin] Payment

## Get Semua payment

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/payments"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
        "id": 48,
        "school_id": "D48797A3-6C81-331B-8BCD-4B9E3A31ABD6",
        "merchant_id": 92,
        "order_no": "5FEAABB737D7D",
        "order_date": "2001-02-19T20:38:16.000000Z",
        "status_updated_at": null,
        "bill_status": "unpaid",
        "total_price": 9673522,
        "tax_price": 967352,
        "shipping_cost": 36209,
        "details": {
            "documentDate": "1977-10-06",
            "signName": "Nama penerima BAST",
            "signPosition": "Jabatan Penerima BAST",
            "signId": "NIP/NIPY Penerima BAST",
            "signPhone": "08123459789",
            "lateCharge": 20000,
            "lateChargeNote": "terlambat 20 Hari",
            "totalQty": 40,
            "totalPrice": 9663522,
            "taxPrice": 966352
        },
        "payment_method_id": 1,
        "payments": {
            "pm1": {
                "date": "1976-07-16 14:57:00",
                "bankOrigin": "BCA",
                "bankAccount": 1866013150,
                "bankDestination": 2,
                "transferred": 10666083,
                "paymentFile": "https://lorempixel.com/640/480/?27600"
            },
            "pm2": {
                "va": "777771729679989",
                "amount": 10666083,
                "expired": "2020-12-01 10:00:00",
                "paid": false
            }
        },
        "payment_date": "1981-03-26T17:22:12.000000Z",
        "payment_transferred": 10666083,
        "bank_mutation_in_id": null,
        "handling_fee": null,
        "handling_fee_details": null,
        "payment_forwarded_date": null,
        "bank_mutation_out_id": null,
        "bill": 10666083,
        "total_order": 10677083,
        "school": {
            "id": "D48797A3-6C81-331B-8BCD-4B9E3A31ABD6",
            "name": "Sit necessitatibus et dicta porro.",
            "details": {
                "sekolah_id": "D48797A3-6C81-331B-8BCD-4B9E3A31ABD6",
                "nama_sekolah": "Sit necessitatibus et dicta porro.",
                "npsn": "12345678",
                "status": "Negeri",
                "bentuk_pendidikan": "SMK",
                "kd_prov": "030000  ",
                "prov": "Prov. Jawa Tengah",
                "kd_kab": "032200  ",
                "kab": "Kab. Semarang",
                "kd_kec": "032207  ",
                "kec": "Kec. Banyubiru",
                "alamat": "JL. RAYA SEKOLAHAN",
                "desa": "Kemambang",
                "kode_pos": "61373",
                "nomor_telepon": "0321491752",
                "email": "sekolah@gmail.com",
                "nama_bendahara_bos": "Bendahara Sekolah",
                "nip_bendahara_bos": "198209242070011457",
                "nama_kepsek": "Kepala Sekolah",
                "hp_kepsek": "08563397781",
                "nip_kepsek": "196503281990031456",
                "email_kepsek": "kepsek@gmail.com",
                "npwp": "005781570602000",
                "lintang": "-7.583800000000",
                "bujur": "112.422900000000",
                "zona": 4
            }
        },
        "bank_mutation_in": null,
        "bank_mutation_out": null,
        "merchant": {
            "id": 92,
            "name": "Veum Ltd",
            "email": "lpollich@dubuque.biz",
            "phone": "08185596325",
            "image": "https://lorempixel.com/200/200/?71537",
            "bank_account": {
                "name": "Veum Ltd",
                "no": 1336386302,
                "bank": "BRI",
                "branch": "East Brando"
            }
        }
    },
    {....}
]
```

endpoint ini digunakan untuk mendapatkan data Payment.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/payments`

## Get payment berdasarkan penjual

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/payments{merchant}/merchant?q&status&page"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
    {
        "id": 48,
        "school_id": "D48797A3-6C81-331B-8BCD-4B9E3A31ABD6",
        "merchant_id": 92,
        "order_no": "5FEAABB737D7D",
        "order_date": "2001-02-19T20:38:16.000000Z",
        "status_updated_at": null,
        "bill_status": "unpaid",
        "total_price": 9673522,
        "tax_price": 967352,
        "shipping_cost": 36209,
        "details": {
            "documentDate": "1977-10-06",
            "signName": "Nama penerima BAST",
            "signPosition": "Jabatan Penerima BAST",
            "signId": "NIP/NIPY Penerima BAST",
            "signPhone": "08123459789",
            "lateCharge": 20000,
            "lateChargeNote": "terlambat 20 Hari",
            "totalQty": 40,
            "totalPrice": 9663522,
            "taxPrice": 966352
        },
        "payment_method_id": 1,
        "payments": {
            "pm1": {
                "date": "1976-07-16 14:57:00",
                "bankOrigin": "BCA",
                "bankAccount": 1866013150,
                "bankDestination": 2,
                "transferred": 10666083,
                "paymentFile": "https://lorempixel.com/640/480/?27600"
            },
            "pm2": {
                "va": "777771729679989",
                "amount": 10666083,
                "expired": "2020-12-01 10:00:00",
                "paid": false
            }
        },
        "payment_date": "1981-03-26T17:22:12.000000Z",
        "payment_transferred": 10666083,
        "bank_mutation_in_id": null,
        "handling_fee": null,
        "handling_fee_details": null,
        "payment_forwarded_date": null,
        "bank_mutation_out_id": null,
        "bill": 10666083,
        "total_order": 10677083,
        "school": {
            "id": "D48797A3-6C81-331B-8BCD-4B9E3A31ABD6",
            "name": "Sit necessitatibus et dicta porro.",
            "details": {
                "sekolah_id": "D48797A3-6C81-331B-8BCD-4B9E3A31ABD6",
                "nama_sekolah": "Sit necessitatibus et dicta porro.",
                "npsn": "12345678",
                "status": "Negeri",
                "bentuk_pendidikan": "SMK",
                "kd_prov": "030000  ",
                "prov": "Prov. Jawa Tengah",
                "kd_kab": "032200  ",
                "kab": "Kab. Semarang",
                "kd_kec": "032207  ",
                "kec": "Kec. Banyubiru",
                "alamat": "JL. RAYA SEKOLAHAN",
                "desa": "Kemambang",
                "kode_pos": "61373",
                "nomor_telepon": "0321491752",
                "email": "sekolah@gmail.com",
                "nama_bendahara_bos": "Bendahara Sekolah",
                "nip_bendahara_bos": "198209242070011457",
                "nama_kepsek": "Kepala Sekolah",
                "hp_kepsek": "08563397781",
                "nip_kepsek": "196503281990031456",
                "email_kepsek": "kepsek@gmail.com",
                "npwp": "005781570602000",
                "lintang": "-7.583800000000",
                "bujur": "112.422900000000",
                "zona": 4
            }
        },
        "bank_mutation_in": null,
        "bank_mutation_out": null
    },
    {....}
]
```

endpoint ini digunakan untuk mendapatkan data Payment berdasarkan penjual.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/payments/{merchant}/merchant?q&status&page`

## Post verifikasi pesanan

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{order}/verify"
-H 'Content-Type: application/json'
-d '{
    "system_bank_id": "2",
    "client_bank": {
        "bank": "baru",
        "name": "baru",
        "no": "12345"
    },
    "transferred": "1",
    "transferred_at": "2020-12-29 11:08:11",
    "note": "",
    "bank_mutation_id": "",
    "is_valid": "1"
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Pembayaran Berhasil diverifikasi."
}
```

endpoint ini digunakan untuk verifikasi pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{order}/verify`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
system_bank_id | null | true | sistem bank
client_bank.bank | null | true | bank
client_bank.name | null | true | nama bank
client_bank.no | null | true | no. bank
transferred | null | true | status transfer
transferred_at | null | true | tanggal transfer
note | null | true | catatan
bank_mutation_id | null | true | mutasi bank
is_valid | null | true | valid

## Post verifikasi ulang pesanan

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{order}/reverify"
-H 'Content-Type: application/json'
-d '{
    "system_bank_id": "2",
    "client_bank": {
        "bank": "baru 2",
        "name": "baru 2",
        "no": "12345"
    },
    "transferred": "1",
    "transferred_at": "2020-12-29 11:08:11",
    "note": "",
    "bank_mutation_id": "",
    "is_valid": "1"
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Pembayaran Berhasil diverifikasi ulang"
}
```

endpoint ini digunakan untuk verifikasi ulang pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{order}/reverify`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
system_bank_id | null | true | sistem bank
client_bank.bank | null | true | bank
client_bank.name | null | true | nama bank
client_bank.no | null | true | no. bank
transferred | null | true | status transfer
transferred_at | null | true | tanggal transfer
note | null | true | catatan
bank_mutation_id | null | true | mutasi bank
is_valid | null | true | valid

## Post biaya admin pesanan

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{order}/handling-fees"
-H 'Content-Type: application/json'
-d '{
    "free": "0",
    "fees": {
        "name": "baru 2",
        "amount": "12345"
    }
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Biaya Penanganan Berhasil disimpan"
}
```

endpoint ini digunakan untuk verifikasi biaya penanganan pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{order}/handling-fees`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
free | null | true | status biaya pengiriman
fees.name | null | true | nama pengiriman
fees.amount | null | true | biaya pengiriman

## Post pesanan forwarded

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/payments/{merchant}/forward"
-H 'Content-Type: application/json'
-d '{
    "orders": {
        "id": "1"
    }, 
    "note": "",
    "system_bank_id": "1", 
    "transferred_at": "2020-12-29 11:08:11"
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Pembayaran Berhasil diteruskan ke Penjual."
}
```

endpoint ini digunakan untuk verifikasi biaya penanganan pesanan.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/payments/{merchant}/forward`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
orders.id | null | true | pesanan
note | null | true | catatan
system_bank_id | null | true | sistem bank
transferred_at | null | true | tanggal