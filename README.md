# Demo CI/CD dengan GitHub Actions

Project sederhana untuk mendemonstrasikan alur kerja CI/CD (Continuous Integration/Continuous Deployment) menggunakan GitHub Actions.

## Tujuan
Tujuan dari project ini adalah untuk memberikan edukasi mengenai otomatisasi testing pada setiap perubahan kode.

## Cara Menjalankan Test
```bash
npm install
npm test
```

## Penjelasan Workflow
Setiap kali ada `push` ke branch `main`, GitHub Actions akan:
1. Menjalankan lingkungan Ubuntu.
2. Mengambil source code dari repository.
3. Menginstall dependensi Node.js.
4. Menjalankan unit test yang ada.

Jika test sukses, status workflow akan **hijau** (pass). Jika test gagal, status akan **merah** (fail).

## Skenario Demo Presentasi

### Demo Success
* Lakukan perubahan normal dan push.
* GitHub Actions akan memberikan hasil status sukses.

### Demo Failure
* Ubah ekspektasi pada `sum.test.js` menjadi `toBe(5)`.
* Push ke repository.
* GitHub Actions akan gagal (merah) karena testing tidak sesuai dengan ekspektasi.
* Pesan: "CI membantu menghentikan bug sebelum masuk production."
