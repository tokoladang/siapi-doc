# Autentikasi

Kami Menggunakan dua Jenis Autentikasi untuk dapat mengakses API. yang pertama menggunakan [Session API](/#session-api) yang hanya dipakai oleh Aplikasi Web Internal Kami. dan yang kedua menggunakan [API Token](/#api-token) yang dapat dipakai oleh Aplikasi Mobile atau aplikasi pihak ketiga.

<aside class="notice">
Setiap API endpoint selain type user <em>public</em> membutuhkan Autentikasi.
</aside>

# Session API

Autentikasi dengan Session API harus memanggil endpoint ini terlebih dahulu sebelum login. untuk mendaftarkan sesi ke server yang nantinya akan disimpan di cookies.

### HTTP Request

`GET https://siapi.siplah.tokoladang.co.id/csrf-cookies`


# API Token
