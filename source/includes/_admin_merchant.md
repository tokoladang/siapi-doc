# [Admin] Toko

## Get Semua Toko

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
        "id": 1,
        "name": "Rosenbaum Inc",
        "email": "kamryn.hills@runolfsdottir.com",
        "address": "54078 Clovis Pines\nPort Dwightstad, ND 63832-2686",
        "rating": 5,
        "verified_at": null,
        "suspend": false,
        "status": "unverified"
    },
    {....}
]
```

endpoint ini digunakan untuk mendapatkan data Toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants`

## Get salah satu toko

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/merchants/{merchant}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "id": 2,
    "name": "Hills, Roob and Reinger",
    "address": "56793 Mills Station\nSavannahborough, NH 85389",
    "province_id": "220000",
    "city_id": "220200",
    "district_id": "220205",
    "village_id": "220205AI",
    "postal_code": "66810-3086",
    "longitude": null,
    "latitude": null,
    "slogan": "Quo iusto magni et voluptas.",
    "note": "Ut aut nobis quasi alias omnis.",
    "type": 1,
    "suspend": false,
    "enabled": true,
    "slug": "hills-roob-and-reinger",
    "image": "https://lorempixel.com/200/200/?85422",
    "deleted_at": null,
    "verified_at": null,
    "rating": 5,
    "review_total": 15,
    "review_count": 3,
    "couriers": "jne:jnt",
    "is_umkm": 0,
    "qualified": 1,
    "business_category": "kecil",
    "email": "mraz.demond@murray.com",
    "phone": "08173496730",
    "seller_type": "individual",
    "main_category": null,
    "is_pkp": 0,
    "documents": null,
    "bank_account": {
        "name": "Hills, Roob and Reinger",
        "no": 1974063211,
        "bank": "MANDIRI",
        "branch": "Barrychester"
    },
    "sosmed": null,
    "signature": null,
    "email_verified_at": null,
    "created_by": null,
    "updated_by": null,
    "created_at": "2020-12-29T04:08:08.000000Z",
    "updated_at": "2020-12-29T04:08:08.000000Z",
    "user_id": null
}
```

endpoint ini digunakan untuk mendapatkan data salah satu Toko.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants/{merchant}`

## Post verifikasi toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/verify"
-H 'Content-Type: application/json'
-d '{
    "id": "2"
}'
```
> Contoh Json Response :

```json
{
    "id": 2,
    "name": "Hills, Roob and Reinger",
    "address": "56793 Mills Station\nSavannahborough, NH 85389",
    "province_id": "220000",
    "city_id": "220200",
    "district_id": "220205",
    "village_id": "220205AI",
    "postal_code": "66810-3086",
    "longitude": null,
    "latitude": null,
    "slogan": "Quo iusto magni et voluptas.",
    "note": "Ut aut nobis quasi alias omnis.",
    "type": 1,
    "suspend": false,
    "enabled": true,
    "slug": "hills-roob-and-reinger",
    "image": "https://lorempixel.com/200/200/?85422",
    "deleted_at": null,
    "verified_at": "2020-12-29T04:30:31.000000Z",
    "rating": 5,
    "review_total": 15,
    "review_count": 3,
    "couriers": "jne:jnt",
    "is_umkm": 0,
    "qualified": 1,
    "business_category": "kecil",
    "email": "mraz.demond@murray.com",
    "phone": "08173496730",
    "seller_type": "individual",
    "main_category": null,
    "is_pkp": 0,
    "documents": null,
    "bank_account": {
        "name": "Hills, Roob and Reinger",
        "no": 1974063211,
        "bank": "MANDIRI",
        "branch": "Barrychester"
    },
    "sosmed": null,
    "signature": null,
    "email_verified_at": null,
    "created_by": null,
    "updated_by": null,
    "created_at": "2020-12-29T04:08:08.000000Z",
    "updated_at": "2020-12-29T04:30:31.000000Z",
    "user_id": null
}
```

endpoint ini digunakan untuk memverifikasi Toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/verify`


### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | null | true | ID Toko

## Post suspend toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/suspend"
-H 'Content-Type: application/json'
-d '{
    "id": "2"
}'
```
> Contoh Json Response :

```json
{
    "id": 2,
    "name": "Hills, Roob and Reinger",
    "address": "56793 Mills Station\nSavannahborough, NH 85389",
    "province_id": "220000",
    "city_id": "220200",
    "district_id": "220205",
    "village_id": "220205AI",
    "postal_code": "66810-3086",
    "longitude": null,
    "latitude": null,
    "slogan": "Quo iusto magni et voluptas.",
    "note": "Ut aut nobis quasi alias omnis.",
    "type": 1,
    "suspend": true,
    "enabled": true,
    "slug": "hills-roob-and-reinger",
    "image": "https://lorempixel.com/200/200/?85422",
    "deleted_at": null,
    "verified_at": "2020-12-29T04:30:31.000000Z",
    "rating": 5,
    "review_total": 15,
    "review_count": 3,
    "couriers": "jne:jnt",
    "is_umkm": 0,
    "qualified": 1,
    "business_category": "kecil",
    "email": "mraz.demond@murray.com",
    "phone": "08173496730",
    "seller_type": "individual",
    "main_category": null,
    "is_pkp": 0,
    "documents": null,
    "bank_account": {
        "name": "Hills, Roob and Reinger",
        "no": 1974063211,
        "bank": "MANDIRI",
        "branch": "Barrychester"
    },
    "sosmed": null,
    "signature": null,
    "email_verified_at": null,
    "created_by": null,
    "updated_by": null,
    "created_at": "2020-12-29T04:08:08.000000Z",
    "updated_at": "2020-12-29T04:35:51.000000Z",
    "user_id": null
}
```

endpoint ini digunakan untuk suspend Toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/suspend`


### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | null | true | ID Toko

## Post unsuspend toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/unsuspend"
-H 'Content-Type: application/json'
-d '{
    "id": "2"
}'
```
> Contoh Json Response :

```json
{
    "id": 2,
    "name": "Hills, Roob and Reinger",
    "address": "56793 Mills Station\nSavannahborough, NH 85389",
    "province_id": "220000",
    "city_id": "220200",
    "district_id": "220205",
    "village_id": "220205AI",
    "postal_code": "66810-3086",
    "longitude": null,
    "latitude": null,
    "slogan": "Quo iusto magni et voluptas.",
    "note": "Ut aut nobis quasi alias omnis.",
    "type": 1,
    "suspend": false,
    "enabled": true,
    "slug": "hills-roob-and-reinger",
    "image": "https://lorempixel.com/200/200/?85422",
    "deleted_at": null,
    "verified_at": "2020-12-29T04:30:31.000000Z",
    "rating": 5,
    "review_total": 15,
    "review_count": 3,
    "couriers": "jne:jnt",
    "is_umkm": 0,
    "qualified": 1,
    "business_category": "kecil",
    "email": "mraz.demond@murray.com",
    "phone": "08173496730",
    "seller_type": "individual",
    "main_category": null,
    "is_pkp": 0,
    "documents": null,
    "bank_account": {
        "name": "Hills, Roob and Reinger",
        "no": 1974063211,
        "bank": "MANDIRI",
        "branch": "Barrychester"
    },
    "sosmed": null,
    "signature": null,
    "email_verified_at": null,
    "created_by": null,
    "updated_by": null,
    "created_at": "2020-12-29T04:08:08.000000Z",
    "updated_at": "2020-12-29T04:36:22.000000Z",
    "user_id": null
}
```

endpoint ini digunakan untuk unsuspend Toko.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/unsuspend`


### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | null | true | ID Toko