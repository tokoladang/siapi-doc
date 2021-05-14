# [Seller] Merchant

Merchant digunakan untuk melihat data toko, membuat data toko, dan merubah data toko. 

<aside class="notice">
Memerlukan Authentikasi sebagai seller.
</aside>

## DATA Merchant

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
   "id": 371,
    "name": "Merchant Satu",
    "address": "Alamat Merchant",
    "province_id": "220000",
    "city_id": "220200",
    "district_id": "220205",
    "village_id": "220205AI",
    "postal_code": "67165",
}
```
endpoint ini digunakan untuk mendapatkan data Toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/seller/merchants/{id}`


## Post Tambah Toko

> jenis: seller

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/seller/merchants"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name" : "Merchant Satu",
        "address" : "Alamat Merchant",
        "province_id" : "220000",
        "city_id" : "220200",
        "district_id" : "220205",
        "village_id" : "220205AI",
        "postal_code" : "67165",
        "slogan" : "Anda Senang Kami Senang",
        "note" : "Toko Buka Setiap Hari",
        "image" : "merchant/17/profile/MeQ3oSOHpLnaw5ykBC3CTe7z4OLXGrqTntPd37Th.jpeg",
        "longitude" : "",
        "latitude" : "",
        "couriers" : "jne:jnt",
        "is_umkm" : false,
        "business_category" : "kecil",
        "phone" : "08123456789",
        "seller_type" : "individual",
        "is_pkp" : false,
        "documents" : {
            "npwp" : {"no" : "", "image" : ""},
            "siup" : {"no" : "", "image" : ""},
            "ktp" : {"no" : "", "image" : ""},
            "pkp" : {"no" : "", "image" : ""}
        },
        "bank_account" : {
            "name" : "Merchant Satu",
            "no" : "123457989",
            "bank" : "BCA",
            "branch" : "surabaya"
        },
        "sosmed" : {"fb" : "merchant", "ig" : "@merchant"},
        "signature" : {
            "name" : "Penjual Satu",
            "position" : "Kepala Toko"
        }
      }'
```

endpoint ini digunakan untuk membuat data toko apabila toko masih belum terdaftar.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/seller/merchants`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | null | true | Nama Toko
address |  | false | Alamat Toko
province_id | null | true | Id Provinsi
city_id | null | true | Id Kota
district_id | null | true | Id Kecamatan
village_id | null | true | Id Desa
postal_code |  | false | Kode Pos
image |  | false | path Gambar
longitude |  | false | Longitude Toko
latitude |  | false | Latitude Toko
slogan |  | false | Latitude Toko
note |  | false | Catatan Toko
couriers |  | false | Kurir Toko
is_umkm |  | true | Jenis Toko
business_category |  | true | Kategori Bisnis
phone |  | false | Kategori Bisnis
seller_type |  | false | Tipe Penjual
is_pkp |  | true | Pajak Penjual
documents | null | true | Dokument Penjual
bank_account | null | true | Akun bank Penjual
sosmed | null | false | Akun Sosial Media
signature | null | true | Tanda Penjual

## Put Ubah Toko

> jenis: seller

```shell
curl -X PUT "https://staging.siapi.tokoladang.co.id/seller/merchants/{id}"
  -H 'Content-Type: application/json'
      'Authorization': Bearer {{TOKEN}}
  -d '{
        "name" : "Merchant Satu",
        "address" : "Alamat Merchant",
        "province_id" : "220000",
        "city_id" : "220200",
        "district_id" : "220205",
        "village_id" : "220205AI",
        "postal_code" : "67165",
        "slogan" : "Anda Senang Kami Senang",
        "note" : "Toko Buka Setiap Hari",
        "image" : "merchant/17/profile/MeQ3oSOHpLnaw5ykBC3CTe7z4OLXGrqTntPd37Th.jpeg",
        "longitude" : "",
        "latitude" : "",
        "couriers" : "jne:jnt",
        "is_umkm" : false,
        "business_category" : "kecil",
        "phone" : "08123456789",
        "seller_type" : "individual",
        "is_pkp" : false,
        "documents" : {
            "npwp" : {"no" : "", "image" : ""},
            "siup" : {"no" : "", "image" : ""},
            "ktp" : {"no" : "", "image" : ""},
            "pkp" : {"no" : "", "image" : ""}
        },
        "bank_account" : {
            "name" : "Merchant Satu",
            "no" : "123457989",
            "bank" : "BCA",
            "branch" : "surabaya"
        },
        "sosmed" : {"fb" : "merchant", "ig" : "@merchant"},
        "signature" : {
            "name" : "Penjual Satu",
            "position" : "Kepala Toko"
        }
      }'
```

endpoint ini digunakan untuk merubah data toko.

### HTTP Request

`PUT https://staging.siapi.tokoladang.co.id/seller/merchants/{id}`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
name | null | true | Nama Toko
address |  | false | Alamat Toko
province_id | null | true | Id Provinsi
city_id | null | true | Id Kota
district_id | null | true | Id Kecamatan
village_id | null | true | Id Desa
postal_code |  | false | Kode Pos
image |  | false | path Gambar
longitude |  | false | Longitude Toko
latitude |  | false | Latitude Toko
slogan |  | false | Latitude Toko
note |  | false | Catatan Toko
couriers |  | false | Kurir Toko
is_umkm |  | true | Jenis Toko
business_category |  | true | Kategori Bisnis
phone |  | false | Kategori Bisnis
seller_type |  | false | Tipe Penjual
is_pkp |  | true | Pajak Penjual
documents | null | true | Dokument Penjual
bank_account | null | true | Akun bank Penjual
sosmed | null | false | Akun Sosial Media
signature | null | true | Tanda Penjual
