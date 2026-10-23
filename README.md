# APK-FACTORY

Mengubah satu file HTML menjadi aplikasi Android (APK) secara otomatis lewat GitHub Actions.

## Cara membuat APK

1. Upload file HTML ke halaman utama repo (nama bebas, misalnya `index.html`).
2. Upload `pengaturan.txt` (lihat contoh di bawah).
3. Upload gambar icon PNG ke folder `icons` (disarankan 1024 x 1024, beri ruang kosong di tepi).
4. Upload `debug.keystore` supaya APK baru bisa menimpa versi lama tanpa menghapus data.
5. Tunggu build selesai di tab **Actions** (centang hijau).
6. Buka proses build terbaru, lalu download APK dari bagian **Artifacts**.

Setiap perubahan di repo menjalankan build otomatis. Untuk menjalankan manual: tab **Actions** → **Build APK Umum** → **Run workflow**.

## Isi pengaturan.txt

```
nama=NamaAplikasi
lokasi=ya
screensaver=ya
```

- `nama`: nama aplikasi di HP. Kalau kosong, memakai nama file HTML.
- `lokasi`: `ya` jika aplikasi memakai GPS. Kalau tidak perlu, tulis `tidak`.
- `screensaver`: `ya` jika aplikasi ingin muncul di pilihan screensaver HP.

## Catatan

- Satu repo untuk satu aplikasi. Untuk aplikasi baru, buat repo baru dari template ini.
- Aplikasi harus berupa satu file HTML.
- Jangan hapus atau ganti nama `.github/workflows/build.yml`.
