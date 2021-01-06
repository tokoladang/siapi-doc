# [Buyer] Pemesanan

## Pemesanan barang

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/carts/checkout"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{"couriers": [
        {
            "merchant_id": 92,
            "courier": {
                "name": "JNE",
                "etd": "2-3",
                "cost": "5000"
            }
        }
    ],
    "funding_sources": [
        {
            "merchant_id": 92,
            "funding_source": {
                "kode_sumber_dana": "BOSE00110",
                "sumber_dana": "BOS Reguler"
            }
        }
    ],
    "notes": [
        {
            "merchant_id": 92,
            "note": "Mohon Pengemasan yang Baik"
        }
    ]
}'
```

endpoint ini digunakan untuk melakukan pemesanan barang barang.

`POST https://staging.siapi.tokoladang.co.id/buyer/carts/checkout`

### Query Body

| Parameter      | Default | required | Deskripsi              |
| -------------- | ------- | -------- | ---------------------- |
| merchant_id    |         | true     | ID Toko                |
| courier        | null    | true     | nama kurir             |
| funding_source |         | true     | sumber dana            |
| note           | null    | true     | catatan kepada penjual |

## Menerima tawaran batas waktu toko

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/75/process"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "accept": "1",
}'
```

endpoint ini digunakan untuk menerima tawaran batas waktu toko.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/process`

### Query Body

| Parameter | Default | required | Deskripsi          |
| --------- | ------- | -------- | ------------------ |
| accept    |         | true     | boolean `0 atau 1` |

## Membatalkan pesanan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/75/cancel"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

endpoint ini digunakan untuk membatalkan pesanan.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/cancel`

## Menerima pesanan

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/75/receive"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

endpoint ini digunakan untuk membatalkan pesanan.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/receive`

## Mengatur BAST

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/75/bast"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "bast": {
        "documentDate": "2021-01-04 10:44:08",
        "signName": "Nama penerima BAST",
        "signPosition": "Jabatan Penerima BAST",
        "signId": "NIP/NIPY Penerima BAST",
        "signPhone": "08123459789"
    },
    "bastItems": [
        {
            "id": "75",
            "quantity": "9"
        }
    ]
}'
```

> response example

```shell
{
    "id": 75,
    "order_no": "5FF02A4940C58",
    "order_date": "2021-01-04T03:44:08.000000Z",
    "customer_id": null,
    "address": null,
    "insured": null,
    "insurance_cost": null,
    "shipping_cost": 40000,
    "payment_method_id": null,
    "payment_date": null,
    "total_weight": 40000,
    "total_qty": 5,
    "total_price": 54450,
    "invoice_no": null,
    "created_by": null,
    "updated_by": null,
    "merchant_id": 92,
    "note": "Mohon Pengemasan yang Baik",
    "customer_address_id": null,
    "courier_service_type": null,
    "bill_status": "unpaid",
    "purchase_status": "received",
    "message_status": null,
    "time_limit": 10,
    "status_updated_at": "2021-01-04T05:08:53.000000Z",
    "reason_cancellation": null,
    "courier_receipt": "RESINO987631452",
    "invoice_file": null,
    "payment_bank_origin": null,
    "payment_account_no": null,
    "payment_file": null,
    "payment_forwarded_date": null,
    "tax_price": 5445,
    "funding_source": "BOSE00110",
    "bank_destination_id": null,
    "compare_id": null,
    "school_id": "85491D19-0BA8-4946-90E6-2R0R8DFB985R",
    "courier_detail": {
        "name": "JNE",
        "etd": "2-3",
        "cost": "5000"
    },
    "payment_transferred": null,
    "handling_fee": null,
    "handling_fee_details": null,
    "details": {
        "documentDate": "2021-01-04 10:44:08",
        "signName": "Nama penerima BAST",
        "signPosition": "Jabatan Penerima BAST",
        "signId": "NIP/NIPY Penerima BAST",
        "signPhone": "08123459789",
        "totalQty": 5,
        "totalPrice": 54450,
        "taxPrice": 5445
    },
    "bank_mutation_in_id": null,
    "bank_mutation_out_id": null,
    "payments": null,
    "funding_source_ws": {
        "kode_sumber_dana": "BOSE00110",
        "sumber_dana": "BOS Reguler"
    },
    "created_at": "2021-01-02T08:09:45.000000Z",
    "updated_at": "2021-01-04T05:54:38.000000Z",
    "customer_order_items": [
        {
            "id": 281,
            "product_id": 307,
            "item_no": null,
            "product_name": "Arwana Biru",
            "product_image": "merchant/17/profile/E6cMULPCZMcWcMtNNiP8MmqeCqdSIbAWYKMRMTYT.png",
            "quantity": 5,
            "price": 10890,
            "total_price": 54450,
            "customer_order_id": 75,
            "negotiation_id": null,
            "tax_price": 5445,
            "bast": null,
            "created_by": null,
            "updated_by": null,
            "created_at": "2021-01-02T08:09:45.000000Z",
            "updated_at": "2021-01-02T08:09:45.000000Z"
        }
    ],
    "school": {
        "id": "85491D19-0BA8-4946-90E6-2R0R8DFB985R",
        "name": "SEKOLAH CONTOH",
        "details": {
            "sekolah_id": "85491D19-0BA8-4946-90E6-2R0R8DFB985R",
            "nama_sekolah": "SEKOLAH CONTOH",
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
            "zona": "1"
        },
        "funding_sources": null,
        "created_at": "2020-12-29T02:59:50.000000Z",
        "updated_at": "2020-12-29T02:59:50.000000Z"
    },
    "merchant": {
        "id": 92,
        "name": "O'Conner-Hackett",
        "address": "647 Hickle Ville Apt. 615\nLake Alecberg, DE 12393",
        "province_id": "220000",
        "city_id": "220200",
        "district_id": "220205",
        "village_id": "220205AI",
        "postal_code": "25626-2367",
        "longitude": null,
        "latitude": null,
        "slogan": "Sint pariatur voluptas ratione quaerat.",
        "note": "Est voluptatem repellendus vel laborum pariatur.",
        "type": 1,
        "suspend": false,
        "enabled": true,
        "slug": "oconner-hackett",
        "image": "https://lorempixel.com/200/200/?71869",
        "deleted_at": null,
        "verified_at": null,
        "rating": 5,
        "review_total": 15,
        "review_count": 3,
        "couriers": "jne:jnt",
        "is_umkm": 0,
        "qualified": 1,
        "business_category": "kecil",
        "email": "sven.borer@kulas.org",
        "phone": "08151358355",
        "seller_type": "individual",
        "main_category": null,
        "is_pkp": 0,
        "documents": null,
        "bank_account": {
            "name": "O'Conner-Hackett",
            "no": 1876478800,
            "bank": "BNI",
            "branch": "Gaylordport"
        },
        "sosmed": null,
        "signature": null,
        "email_verified_at": null,
        "created_by": null,
        "updated_by": null,
        "created_at": "2020-12-29T02:03:30.000000Z",
        "updated_at": "2020-12-29T02:03:30.000000Z",
        "user_id": null
    }
}
```

endpoint ini digunakan untuk mengatur BAST.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/bast`

### Query Body

| Parameter      | Default | required | Deskripsi                   |
| -------------- | ------- | -------- | --------------------------- |
| documentDate   |         | true     | Tanggal Dokumen             |
| signName       |         | true     | Nama Penerima BAST          |
| signPosition   |         | true     | Jabatan Penerima BAST       |
| signId         |         | true     | NIP/NIPY Penerima BAST      |
| signPhone      |         | true     | Telepon Penerima BAST       |
| lateCharge     |         | false    | Denda Keterlambatan         |
| lateChargeNote |         | false    | Catatan Denda Keterlambatan |
| id             |         | true     | id bast items               |
| quantity       |         | true     | jumlah bast items           |

## Mengatur pembayaran transfer bank

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/75/receive"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{
    "date": "2021-01-04 12:54:38",
    "bankOrigin": "BNI",
    "bankAccount": "987654321"
    "bankDestination": 2
    "transferred": 54450
    "paymentFile":"school/85491D19-0BA8-4946-90E6-2R0R8DFB985R/KFNoNR2ZnjdBMnH6OnR95sT10zoSGiwoKj0ZoQje.png"
  }'
```

endpoint ini digunakan untuk mengatur pembayaran bank transfer.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/payment1`

### Query Body

| Parameter       | Default | required | Deskripsi              |
| --------------- | ------- | -------- | ---------------------- |
| date            |         | true     | Tanggal Pembayaran     |
| bankOrigin      | null    | true     | Nama Bank              |
| bankAccount     | null    | true     | Akun Bank              |
| bankDestination | null    | true     | Bank Tujuan            |
| transferred     | null    | true     | Jumlah yang ditransfer |
| paymentFile     | null    | true     | Bukti Pembayaran       |

## Mengatur Pembayaran BRIVA

> jenis: buyer

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/buyer/orders/75/payment2"
  -H 'Authorization: Bearer {{TOKEN}}'
  -H 'Content-Type: application/json'
  -d '{}'
```

> response example

```shell
{
    "code": 200,
    "message": "Berhasil Mengatur Pembayaran Briva Virtual Account",
    "data": {
        "pm2": {
            "va": "0695456033",
            "amount": 147811,
            "expired": "2021-01-19 10:14:37",
            "paid": false
        }
    }
}
```

endpoint ini digunakan untuk mengatur pembayaran bank transfer.

`POST https://staging.siapi.tokoladang.co.id/buyer/orders/{$order->id}/payment2`
