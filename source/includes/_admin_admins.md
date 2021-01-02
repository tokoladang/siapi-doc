# [Admin] Admins

## Get Semua Admin

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/admins"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
  {
        "id": 1,
        "name": "Jackie Grimes",
        "email": "super@gmail.com",
        "email_verified_at": "2020-12-29T04:08:07.000000Z",
        "roles": [
            "*"
        ],
        "active": true,
        "created_at": "2020-12-29T04:08:08.000000Z",
        "updated_at": "2020-12-29T04:08:08.000000Z"
    },
    {....}
]
```

endpoint ini digunakan untuk mendapatkan data admin.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/admins`

## Post Admin baru

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/admins"
-H 'Content-Type: application/json'
-d '{
    "name": "new admin",
    "email": "new@demo.id"
    "roles": "*"
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Admin Berhasil ditambahkan",
}
```

endpoint ini digunakan untuk menambah user admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/admins`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
email | null | true | Email Admin
name | null | true | Name Admin
roles | null | true | Rule

## Post ubah role Admin

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/admins/{admin}/update-roles"
-H 'Content-Type: application/json'
-d '{
    "roles": "finance"
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Peran Admin Berhasil diubah",
}
```

endpoint ini digunakan untuk update role admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/admins/{admin}/update-roles`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
roles | null | true | Rule

## Post ubah status Admin

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/admins/{admin}/update-active"
-H 'Content-Type: application/json'
-d '{
    "active": "0"
}'
```
> Contoh Json Response :

```json
{
    "code": 200,
    "message": "Admin Berhasil ditambahkan",
    "data": {
        "email": "new@demo.id",
        "name": "new admin",
        "roles": "*",
        "active": true,
        "updated_at": "2020-12-29T07:03:14.000000Z",
        "created_at": "2020-12-29T07:03:14.000000Z",
        "id": 12
    }
}
```

endpoint ini digunakan untuk mengubah status admin.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/admins/{admin}/update-active`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
active | null | true | status aktif