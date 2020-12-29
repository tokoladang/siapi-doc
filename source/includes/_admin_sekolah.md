# [Admin] Sekolah

## Get Semua Sekolah

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/schools"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
    {
        "id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
        "name": "Distinctio optio quidem vel non est occaecati vel.",
        "details": {
            "sekolah_id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
            "nama_sekolah": "Distinctio optio quidem vel non est occaecati vel.",
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
            "zona": 1
        },
        "funding_sources": [
            {
                "sumber_dana_id": "E802B268-6F57-4C57-A069-8DFA07E1B267",
                "sumber_dana": "BOS Reguler",
                "tahun_sumber_dana": "2020",
                "kode_sumber_dana": "BOSE00110"
            }
        ],
        "created_at": "2020-12-29T04:08:09.000000Z",
        "updated_at": "2020-12-29T04:08:09.000000Z"
    },
    {....}
]
```

endpoint ini digunakan untuk mendapatkan semua data sekolah.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/schools`

## Get salah satu Sekolah

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/schools/{school}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
    "name": "Distinctio optio quidem vel non est occaecati vel.",
    "details": {
        "sekolah_id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
        "nama_sekolah": "Distinctio optio quidem vel non est occaecati vel.",
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
        "zona": 1
    },
    "funding_sources": [
        {
            "sumber_dana_id": "E802B268-6F57-4C57-A069-8DFA07E1B267",
            "sumber_dana": "BOS Reguler",
            "tahun_sumber_dana": "2020",
            "kode_sumber_dana": "BOSE00110"
        }
    ],
    "created_at": "2020-12-29T04:08:09.000000Z",
    "updated_at": "2020-12-29T04:08:09.000000Z"
}
```

endpoint ini digunakan untuk mendapatkan salah satu data sekolah.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/schools/{school}`

## Get customer berdasarkan Sekolah

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/customers/{schoolId}"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
[
    {
        "id": 9,
        "name": "Dr. Marco Turcotte Jr.",
        "username": "xschroeder@example.org",
        "birthday": null,
        "gender": null,
        "email": "xschroeder@example.org",
        "phone": null,
        "enabled": 1,
        "user_id": null,
        "image": null,
        "is_phone_verified": 0,
        "is_email_verified": 0,
        "created_by": null,
        "updated_by": null,
        "school_id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
        "details": {
            "nama": "Buyer",
            "nik": "3516132409850001",
            "nip": "198209242070011457",
            "pengguna_id": "301F2DFD-B6F2-3872-B24C-137B53156BA8",
            "peran_id": "53",
            "peran": "Kepala Sekolah",
            "sekolah_id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
            "kode_wilayah": "032207AB",
            "no_telepon": "08563397781",
            "no_hp": "08563397781",
            "username": "xschroeder@example.org"
        },
        "created_at": "2020-12-29T04:08:09.000000Z",
        "updated_at": "2020-12-29T04:08:09.000000Z"
    }
]
```

endpoint ini digunakan untuk mendapatkan data customer berdasarkan id sekolah.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/customers/{schoolId}`

## Get customer detail

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/customers/{customer}/detail"
-H 'Content-Type: application/json'
-d '{}'
```
> Contoh Json Response :

```json
{
    "id": 9,
    "name": "Dr. Marco Turcotte Jr.",
    "username": "xschroeder@example.org",
    "birthday": null,
    "gender": null,
    "email": "xschroeder@example.org",
    "phone": null,
    "enabled": 1,
    "user_id": null,
    "image": null,
    "is_phone_verified": 0,
    "is_email_verified": 0,
    "created_by": null,
    "updated_by": null,
    "school_id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
    "details": {
        "nama": "Buyer",
        "nik": "3516132409850001",
        "nip": "198209242070011457",
        "pengguna_id": "301F2DFD-B6F2-3872-B24C-137B53156BA8",
        "peran_id": "53",
        "peran": "Kepala Sekolah",
        "sekolah_id": "348D60E0-81E0-3DD7-803F-ADC860EB7D22",
        "kode_wilayah": "032207AB",
        "no_telepon": "08563397781",
        "no_hp": "08563397781",
        "username": "xschroeder@example.org"
    },
    "created_at": "2020-12-29T04:08:09.000000Z",
    "updated_at": "2020-12-29T04:08:09.000000Z"
}
```

endpoint ini digunakan untuk mendapatkan data detail customer.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/customers/{customer}/detail`