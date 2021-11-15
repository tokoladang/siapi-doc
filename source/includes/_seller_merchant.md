# [Seller] Toko

Merchant digunakan untuk melihat data toko, membuat data toko, dan merubah data toko. 

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## DATA Toko

## Get Data Toko

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/merchants/{id}"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
{
  "id": "integer",
  "name": "string",
  "address": "string",
  "branch": {"id": "integer", "code": "string", "name": "string"},
  "province_id": "integer",
  "city_id": "integer",
  "district_id": "integer",
  "village_id": "integer",
  "postal_code": "string",
  "longitude": "string",
  "latitude": "string",
  "slogan": "string",
  "note": "string",
  "type": "string",
  "slug": "string",
  "image": "string",
  "banners": "json",
  "deleted_at": "datetime",
  "verified_at": "datetime",
  "rating": "float",
  "review_total": "integer",
  "review_count": "integer",
  "couriers": "string",
  "is_umkm": "boolean",
  "qualified": "boolean",
  "business_category": "string",
  "email": "string",
  "phone": "string",
  "main_category": "integer",
  "seller_type": "string",
  "documents": "json",
  "bank_account": "json",
  "sosmed": "json",
  "signature": "json",
  "email_verified_at": "datetime",
  "created_by": "string",
  "updated_by": "string",
  "power": "integer",
  "admin_note": "string",
  "status": "string",
  "verified_by": "integer"
}
```
endpoint ini digunakan untuk mendapatkan data Toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/merchants/{id}`

## Get Data Pengguna

> jenis: seller

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/seller/merchants?q=&status=&page="
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
```

> Contoh Json Response :

```json
[
  {
    "created_at": "datetime",
    "email": "string",
    "email_verified_at": "datetime",
    "enabled": "boolean",
    "id": "integer",
    "merchant_id": "integer",
    "name": "string",
    "phone": "string",
    "roles": "json",
    "updated_at": "datetime"
  }
]
```
endpoint ini digunakan untuk mendapatkan data Pengguna.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/merchants?q=&status=&page=`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
q | string | false | kata kunci
status | string | false | status
page | string | false | halaman

## Post Tambah Toko Baru

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/merchants"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "string",
        "slug": "string",
        "address": "string",
        "province_id": "integer",
        "city_id": "integer",
        "district_id": "integer",
        "village_id": "integer",
        "postal_code": "integer",
        "longitude": "string",
        "latitude": "string",
        "slogan": "string",
        "note": "string",
        "image": "string",
        "banners": "json",
        "couriers": "string",
        "is_umkm": "boolean",
        "business_category": "string",
        "phone": "string",
        "type": "string",
        "seller_type": "string",
        "email": "string",
        "admin_note": "string",
        "branch_id": "integer",
        "documents" : {
            "npwp" : {"no" : "integer", "image" : "string"},
            "siup" : {"no" : "integer", "image" : "string"},
            "ktp" : {"no" : "integer", "image" : "string"},
            "pkp" : {"no" : "integer", "image" : "string"}
        },
        "bank_account" : {
            "name" : "string",
            "no" : "string",
            "bank" : "string",
            "branch" : "string"
        },
        "sosmed" : {"fb" : "contoh", "ig" : "contoh"},
        "signature" : {
            "name" : "string",
            "position" : "string"
        }
      }'
```
> Contoh Json Response :

```json
{
  "id": "integer",
  "name": "string",
  "address": "string",
  "branch": {"id": "integer", "code": "string", "name": "string"},
  "province_id": "integer",
  "city_id": "integer",
  "district_id": "integer",
  "village_id": "integer",
  "postal_code": "string",
  "longitude": "string",
  "latitude": "string",
  "slogan": "string",
  "note": "string",
  "type": "string",
  "slug": "string",
  "image": "string",
  "banners": "json",
  "deleted_at": "datetime",
  "verified_at": "datetime",
  "rating": "float",
  "review_total": "integer",
  "review_count": "integer",
  "couriers": "string",
  "is_umkm": "boolean",
  "qualified": "boolean",
  "business_category": "string",
  "email": "string",
  "phone": "string",
  "main_category": "integer",
  "seller_type": "string",
  "documents": "json",
  "bank_account": "json",
  "sosmed": "json",
  "signature": "json",
  "email_verified_at": "datetime",
  "created_by": "string",
  "updated_by": "string",
  "power": "integer",
  "admin_note": "string",
  "status": "string",
  "verified_by": "integer"
}
```
endpoint ini digunakan untuk membuat data toko apabila toko masih belum terdaftar.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/merchants`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Toko
email | string | true | Email Toko
address | string | false | Alamat Toko
province_id | integer | true | Id Provinsi
city_id | integer | true | Id Kota/Kabupaten
district_id | integer | true | Id Kecamatan
village_id | integer | true | Id Desa
postal_code | integer | true | Kode Pos
image | string | false | Gambar Profil
longitude | string | true[ -180 .. 180 ] | Longitude Alamat
latitude | string | true[ -90 .. 90 ] | Latitude Alamat
slogan | string | false | Slogan
note | string | false | Catatan
couriers | string | true | Kurir
is_umkm | boolean | true | Barang UMKM?
business_category | string | true | Kategori Usaha
phone | string | false | No. Telephone Toko
type | string | true | Tipe Toko
seller_type | string | true | Tipe Penjual
documents | json | true | KTP, NPWP, (SIUP & PKP Opsional)
bank_account | json | true | No. Rek, Nama, Bank, Cabang
sosmed | json | false | Sosial Media
signature | json | true | Nama, Posisi (Penanggung Jawab)
banners | json | false | Gambar Banner
branch_id | integer | false | Kode Cabang

## Put Ubah Data Toko

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/merchants/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "string",
        "slug": "string",
        "address": "string",
        "province_id": "integer",
        "city_id": "integer",
        "district_id": "integer",
        "village_id": "integer",
        "postal_code": "integer",
        "longitude": "string",
        "latitude": "string",
        "slogan": "string",
        "note": "string",
        "image": "string",
        "banners": "json",
        "couriers": "string",
        "is_umkm": "boolean",
        "business_category": "string",
        "phone": "string",
        "type": "string",
        "seller_type": "string",
        "email": "string",
        "admin_note": "string",
        "branch_id": "integer",
        "documents" : {
            "npwp" : {"no" : "integer", "image" : "string"},
            "siup" : {"no" : "integer", "image" : "string"},
            "ktp" : {"no" : "integer", "image" : "string"},
            "pkp" : {"no" : "integer", "image" : "string"}
        },
        "bank_account" : {
            "name" : "string",
            "no" : "string",
            "bank" : "string",
            "branch" : "string"
        },
        "sosmed" : {"fb" : "contoh", "ig" : "contoh"},
        "signature" : {
            "name" : "string",
            "position" : "string"
        }
      }'
```
> Contoh Json Response :

```json
{
  "id": "integer",
  "name": "string",
  "address": "string",
  "branch": {"id": "integer", "code": "string", "name": "string"},
  "province_id": "integer",
  "city_id": "integer",
  "district_id": "integer",
  "village_id": "integer",
  "postal_code": "string",
  "longitude": "string",
  "latitude": "string",
  "slogan": "string",
  "note": "string",
  "type": "string",
  "slug": "string",
  "image": "string",
  "banners": "json",
  "deleted_at": "datetime",
  "verified_at": "datetime",
  "rating": "float",
  "review_total": "integer",
  "review_count": "integer",
  "couriers": "string",
  "is_umkm": "boolean",
  "qualified": "boolean",
  "business_category": "string",
  "email": "string",
  "phone": "string",
  "main_category": "integer",
  "seller_type": "string",
  "documents": "json",
  "bank_account": "json",
  "sosmed": "json",
  "signature": "json",
  "email_verified_at": "datetime",
  "created_by": "string",
  "updated_by": "string",
  "power": "integer",
  "admin_note": "string",
  "status": "string",
  "verified_by": "integer"
}
```
endpoint ini digunakan untuk merubah data toko.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/merchants/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Toko
email | string | true | Email Toko
address | string | false | Alamat Toko
province_id | integer | true | Id Provinsi
city_id | integer | true | Id Kota/Kabupaten
district_id | integer | true | Id Kecamatan
village_id | integer | true | Id Desa
postal_code | integer | true | Kode Pos
image | string | false | Gambar Profil
longitude | string | true[ -180 .. 180 ] | Longitude Alamat
latitude | string | true[ -90 .. 90 ] | Latitude Alamat
slogan | string | false | Slogan
note | string | false | Catatan
couriers | string | true | Kurir
is_umkm | boolean | true | Barang UMKM?
business_category | string | true | Kategori Usaha
phone | string | false | No. Telephone Toko
type | string | true | Tipe Toko
seller_type | string | true | Tipe Penjual
documents | json | true | KTP, NPWP, (SIUP & PKP Opsional)
bank_account | json | true | No. Rek, Nama, Bank, Cabang
sosmed | json | false | Sosial Media
signature | json | true | Nama, Posisi (Penanggung Jawab)
banners | json | false | Gambar Banner
branch_id | integer | false | Kode Cabang

## Post Ubah Status Toko

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/merchants/status"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "status": "string"
      }'
```

> Contoh Json Response :

```json
{
  "code": "Kode Respon",
  "message": "Pesan Respon"
}
```
endpoint ini digunakan untuk Mengubah status toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/merchants/status`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | string | true | status toko

## Post Tambah Pengguna Baru

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/merchants/user"
  -H 'Content-Type: application/json',
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name": "string",
        "email": "string",
        "roles": "array"
      }'
```

> Contoh Json Response :

```json
{
  "code": "Kode Respon",
  "message": "Pesan Respon"
}
```
endpoint ini digunakan untuk menambahkan Pengguna Baru.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/merchants/user`

### Query Parameter

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | string | true | Nama Pengguna
email | string | true | Email Pengguna
roles | array | true | Peran
