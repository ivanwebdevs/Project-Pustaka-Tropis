# Dokumentasi API Untuk admin

## Base URL
```
https://pustakatropis.com/api
```

## Endpoint: Get Products
### Endpoint
```
GET /admin/products
```

### Parameters
| Parameter | Type   | Description                    |
|-----------|--------|--------------------------------|
| name      | string | (Optional) Filter berdasarkan nama produk |
| tag       | string | (Optional) Filter berdasarkan tag |
| limit | integer | (Default = 10) Limit Berapa item dalam 1 page|
| page | integer | (Default = 1) page yang akan di baca|

### Response
#### Success Response (200 OK)
```json
{
    "pagination": {
        "prev": null,
        "next": 2,
        "list_prev": [],
        "list_next": [
            2
        ]
    },
    "current_page": 1,
    "total_pages": 2,
    "item_found": 3,
    "curent_item": 2,
    "limit": 2,
    "data": [
        {
            "id": "1",
            "name": "product example 1",
            "tag": "admin,user",
            "image_preview": "image_preview example 1",
            "created_at": "2025-03-13 12:56:50"
        },
        {
            "id": "2",
            "name": "product example 2",
            "tag": "jagung,pohon",
            "image_preview": "image_preview example 2",
            "created_at": "2025-03-13 12:56:50"
        }
    ]
}
```

### Notes
- Jika parameter `name` dan `tag` tidak diberikan, maka semua produk akan ditampilkan.
- Parameter bersifat opsional, sehingga dapat digunakan sesuai kebutuhan.






## Endpoint: Detail Product
### Endpoint
```
GET /admin/products/{id}
```

### Parameters
| Parameter | Type   | Description                    |
|-----------|--------|--------------------------------|
| id      | int | (Required) Pencarian Detail berdasarkan ID product |

### Response
#### Success Response (200 OK)
```json
{
    "id": "1",
    "name": "product example 1",
    "description": "description example 1",
    "tag": "admin,user",
    "image_preview": "image_preview example 1",
    "image_raw": "image_raw example 1",
    "price_type": "fixed",
    "price_start": "1000",
    "price_end": "0",
    "price_fix": "0",
    "created_at": "2025-03-13 12:56:50",
    "updated_at": null
}
```

### Notes
- Jika parameter `name` dan `tag` tidak diberikan, maka semua produk akan ditampilkan.
- Parameter bersifat opsional, sehingga dapat digunakan sesuai kebutuhan.





