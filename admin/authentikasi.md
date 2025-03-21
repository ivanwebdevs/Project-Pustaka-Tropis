# Dokumentasi API: Login Admin

## Endpoint
**POST** `/api/admin/auth/login`

## Deskripsi
Endpoint ini digunakan untuk login ke sistem admin dengan username dan password.

## Parameter

| Parameter   | Tipe    | Wajib | Deskripsi               |
|------------|--------|------|------------------------|
| username   | string | Ya   | Username admin         |
| password   | string | Ya   | Password admin         |

## Contoh Request

### HTTP Request
```http
POST /api/admin/auth/login HTTP/1.1
Host: your-api-domain.com
Content-Type: application/x-www-form-urlencoded

username=admin&password=password123
```

## Response

### Berhasil
**Status Code: 200**
```json
{
    "status": 200,
    "message": "Login berhasil"
}
```

### Gagal
Jika login gagal (misalnya username atau password salah), maka response akan seperti berikut:

**Status Code: 401**
```json
{
    "status": 401,
    "message": "Username atau password salah"
}
```

## Catatan
- Pastikan username dan password yang dikirimkan sesuai dengan yang terdaftar di sistem.
- Gunakan HTTPS untuk keamanan data.

