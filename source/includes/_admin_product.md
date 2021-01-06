# [Admin]Produk

## Get semua Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products?q=&status="
-H 'Content-Type: application/json'
-d '{}'
```

Contoh Json Response :

```json
[
  {
        "id": 1,
        "sku": "SKU5FEAABAA5D151",
        "upc": null,
        "ean": null,
        "name": "Culpa totam laudantium laudantium sit.",
        "description": "Occaecati eaque aperiam laudantium accusamus. Ut a quia illo sequi culpa. Est expedita vel placeat cupiditate ut. Sunt ducimus nihil voluptatem minima ullam nihil ut.",
        "product_category_id": 1,
        "brand_id": null,
        "merchant_id": 66,
        "price": 41640902,
        "qty_available": 37,
        "qty_sell": 60,
        "status": "unavailable",
        "slug": "culpa-totam-laudantium-laudantium-sit",
        "weight": 914,
        "is_secondhand": true,
        "discount": 1,
        "taxed": false,
        "price_zone_1": 41641902,
        "price_zone_2": 41642902,
        "price_zone_3": 41643902,
        "price_zone_4": 41644902,
        "price_zone_5": 41645902,
        "wholesales": [
            {
                "quantity": 10,
                "price": 41639902
            },
            {
                "quantity": 20,
                "price": 41638902
            }
        ],
        "isbn": "9793846863434",
        "rating": 5,
        "review_total": 500,
        "review_count": 100,
        "with_shipping_cost": true,
        "image": "https://lorempixel.com/640/480/?51590",
        "images": [
            "https://lorempixel.com/640/480/?51590",
            "https://lorempixel.com/640/480/?58979"
        ],
        "kind": "Buku",
        "merchant_storage_id": null,
        "is_goods": true,
        "is_umkm": true,
        "is_domestic": true,
        "qualified": true,
        "created_by": null,
        "updated_by": null,
        "created_at": "2020-12-29T04:08:10.000000Z",
        "updated_at": "2020-12-29T04:08:10.000000Z"
    },
    {...}
]
```

endpoint ini digunakan untuk mendapatkan data produk.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products?q=&status=`

## Get salah satu Produk

> jenis: admin

```shell
curl -X GET "https://staging.siapi.tokoladang.co.id/admin/products/{id}"
-H 'Content-Type: application/json'
-d '{}'
```

Contoh Json Response :

```json
{
    "id": 1,
    "sku": "SKU5FEAABAA5D151",
    "upc": null,
    "ean": null,
    "name": "Culpa totam laudantium laudantium sit.",
    "description": "Occaecati eaque aperiam laudantium accusamus. Ut a quia illo sequi culpa. Est expedita vel placeat cupiditate ut. Sunt ducimus nihil voluptatem minima ullam nihil ut.",
    "product_category_id": 1,
    "brand_id": null,
    "merchant_id": 66,
    "price": 41640902,
    "qty_available": 37,
    "qty_sell": 60,
    "status": "unavailable",
    "slug": "culpa-totam-laudantium-laudantium-sit",
    "weight": 914,
    "is_secondhand": true,
    "discount": 1,
    "taxed": false,
    "price_zone_1": 41641902,
    "price_zone_2": 41642902,
    "price_zone_3": 41643902,
    "price_zone_4": 41644902,
    "price_zone_5": 41645902,
    "wholesales": [
        {
            "quantity": 10,
            "price": 41639902
        },
        {
            "quantity": 20,
            "price": 41638902
        }
    ],
    "isbn": "9793846863434",
    "rating": 5,
    "review_total": 500,
    "review_count": 100,
    "with_shipping_cost": true,
    "image": "https://lorempixel.com/640/480/?51590",
    "images": [
        "https://lorempixel.com/640/480/?51590",
        "https://lorempixel.com/640/480/?58979"
    ],
    "kind": "Buku",
    "merchant_storage_id": null,
    "is_goods": true,
    "is_umkm": true,
    "is_domestic": true,
    "qualified": true,
    "created_by": null,
    "updated_by": null,
    "created_at": "2020-12-29T04:08:10.000000Z",
    "updated_at": "2020-12-29T04:08:10.000000Z"
}
```

endpoint ini digunakan untuk mendapatkan data produk berdasarkan id.

### HTTP Request

`GET https://staging.siapi.tokoladang.co.id/admin/products/{id}`

## Update status produk

> jenis: admin

```shell
curl -X POST "https://staging.siapi.tokoladang.co.id/admin/products/{id}/status"
-H 'Content-Type: application/json'
-d '{
    "status": "unavailable"
}'
```

Contoh Json Response :

```json
{
    "code": 200,
    "message": "Status produk berhasil diubah."
}
```

endpoint ini digunakan untuk mengubah status produk.

### HTTP Request

`POST https://staging.siapi.tokoladang.co.id/admin/products/{id}/status`

### Query Body

Parameter | Default | required | Deskripsi
--------- | ------- | -------- | -----------
status | null | true | Status produk