# Login admin
```
username    : Admin
password    : admin
```

# Login dokter
password adalah username, jadi password dimasukan nama dokter nya

## Informasi Login
Jika Anda mengalami kendala saat login, Anda dapat melakukan perubahan langsung pada database untuk memastikan username dan password sesuai. Berikut adalah langkah-langkahnya:

### Langkah-Langkah Mengubah Username dan Password di Database
1. **Akses Database:**
   - Buka phpMyAdmin atau tool database yang Anda gunakan.
   - Pilih database proyek Anda.

2. **Cari Tabel User:**
   - Navigasikan ke tabel `user` (atau nama tabel yang menyimpan data login).

3. **Edit Data Login:**
   - Pilih record (baris) pengguna yang ingin diubah.
   - Klik tombol **Edit** pada record tersebut.

4. **Ubah Username dan Password:**
   - **Kolom `username`:** Masukkan username baru yang diinginkan.
   - **Kolom `password`:** Masukkan password baru dalam format *md5* menggunakan fungsi bawaan database.
     Contoh SQL untuk mengubah password:
     ```sql
     UPDATE user SET password = MD5('passwordbaru') WHERE id = 1;
     ```
     Gantilah `'passwordbaru'` dengan password yang Anda inginkan.

5. **Simpan Perubahan:**
   - Klik **Save** atau jalankan perintah SQL untuk menyimpan perubahan.

6. **Coba Login Kembali:**
   - Gunakan kombinasi username dan password yang baru saja Anda ubah.

---

### Contoh Default Login
Berikut adalah informasi login default yang dapat digunakan:
- **Admin:**
  - Username: `Admin`
  - Password: `admin`
- **Dokter:**
  - Username: `Ifan`
  - Password: `Semarang`
- **Pasien:**
  - Username: `Adi`
  - Password: `Semarang`

> Jika username atau password ini tidak berfungsi, silakan ikuti langkah-langkah di atas untuk mengubah data login di database.

---

Semoga informasi ini membantu Anda mengatasi kendala login!
