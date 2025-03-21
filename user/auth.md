# Dokumentasi API Autentikasi

## Endpoint: `/api/user/auth`

### 1. Login
**Endpoint:** `POST /api/user/auth/login`

**Deskripsi:**
Digunakan untuk melakukan login pengguna.

**Request Body:**
```json
{
    "email": "user@example.com",
    "password": "password123"
}
```

**Response Sukses:**
```json
{
    "status": 200,
    "message": "Login berhasil"
}
```

**Response Gagal:**
- Jika email atau password salah:
```json
{
    "status": 400,
    "message": "Password salah"
}
```
- Jika email tidak ditemukan:
```json
{
    "status": 400,
    "message": "User tidak ditemukan"
}
```
- Jika sudah login sebelumnya:
```json
{
    "status": 200,
    "message": "Anda sudah login"
}
```

---

### 2. Cek Status Login
**Endpoint:** `GET /api/user/auth/check`

**Deskripsi:**
Digunakan untuk mengecek apakah pengguna sudah login atau belum.

**Response Jika Sudah Login:**
```json
{
    "status": 200,
    "message": "Anda sudah login"
}
```

**Response Jika Belum Login:**
```json
{
    "status": 400,
    "message": "Anda belum login"
}
```

---

### 3. Logout
**Endpoint:** `DELETE /api/user/auth/logout`

**Deskripsi:**
Digunakan untuk melakukan logout pengguna.

**Response Sukses:**
```json
{
    "status": 200,
    "message": "Berhasil logout"
}
```

**Response Jika Tidak Login:**
```json
{
    "status": 400,
    "message": "Anda tidak login"
}
```

