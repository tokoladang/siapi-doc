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
{
  "data": {....}
}
```

endpoint ini digunakan untuk mendapatkan data Toko.

## HTTP Request

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
  "data": {....}
}
```

endpoint ini digunakan untuk mendapatkan data salah satu Toko.

## HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/merchants/{merchant}`

## Post verifikasi toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/verify"
-H 'Content-Type: application/json'
-d '{
    "id": "1"
}'
```
> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk memverifikasi Toko.

## HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/verify`


## Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | null | true | ID Toko

## Post suspend toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/suspend"
-H 'Content-Type: application/json'
-d '{
    "id": "1"
}'
```
> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk suspend Toko.

## HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/suspend`


## Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | null | true | ID Toko

## Post unsuspend toko

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/merchants/unsuspend"
-H 'Content-Type: application/json'
-d '{
    "id": "1"
}'
```
> Contoh Json Response :

```json
{
  "data": {....}
}
```

endpoint ini digunakan untuk unsuspend Toko.

## HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/merchants/unsuspend`


## Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
id | null | true | ID Toko