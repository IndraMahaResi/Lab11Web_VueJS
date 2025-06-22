📘 Dokumentasi PRAKTIKUM 11 : VueJS
🙋‍♂️ Identitas
Nama: Indra Maha Resi

NIM: [312310044]

Kelas: [TI.23.C1]

Nama Project: PRAKTIKUM WEB2

📁 Deskripsi Singkat
Proyek ini dibuat untuk memenuhi tugas Praktikum Web2, khususnya berfokus pada pengembangan antarmuka frontend interaktif menggunakan VueJS 3 yang terintegrasi dengan API RESTful CodeIgniter 4 yang sudah ada (dari Praktikum 10). Ini mendemonstrasikan bagaimana aplikasi frontend terpisah dapat mengonsumsi data dan melakukan operasi CRUD melalui API.

📸 Dokumentasi Langkah-langkah
Semua screenshot disimpan dalam folder Dokumentasi/ di dalam proyek.

🧱 Praktikum 11: Frontend dengan VueJS 3
Praktikum ini mengimplementasikan antarmuka pengguna interaktif untuk manajemen artikel menggunakan VueJS 3, berinteraksi dengan API RESTful CodeIgniter 4.

Langkah 1: Persiapan dan Struktur Proyek VueJS
Buat folder baru bernama lab8_vuejs di dalam docroot web server Anda (misalnya htdocs).

Di dalam folder tersebut, buat struktur direktori berikut:

lab8_vuejs/
├── index.html
├── assets/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── app.js

Pastikan Anda memiliki akses internet untuk memuat CDN VueJS dan Axios.

Langkah 2: Konfigurasi index.html
Buat file index.html di lab8_vuejs/.

Sertakan CDN untuk VueJS 3 dan Axios di bagian <head>.

Link ke assets/css/style.css dan assets/js/app.js.

Siapkan elemen <div id="app"> sebagai root aplikasi VueJS Anda.

Tambahkan elemen HTML untuk tabel artikel, tombol "Tambah Data", dan struktur modal form untuk tambah/ubah data.

Langkah 3: Styling dengan style.css
Buat file style.css di lab8_vuejs/assets/css/.

Tambahkan kode CSS untuk mengatur tampilan tabel, form modal, tombol, dan elemen lainnya agar lebih menarik dan responsif.

Langkah 4: Logika Aplikasi dengan app.js (VueJS)
Buat file app.js di lab8_vuejs/assets/js/.

Tentukan apiUrl yang menunjuk ke API RESTful CodeIgniter Anda (dari Praktikum 10). Pastikan URL ini benar dan API Anda sudah berjalan!

Definisikan data() reactive untuk artikel, formData, showForm, formTitle, dan statusOptions.

Implementasikan mounted() untuk memuat data artikel pertama kali saat aplikasi dimuat.

Buat methods untuk:

loadData(): Mengambil data artikel dari API menggunakan Axios.

statusText(): Mengubah nilai status (misal 0/1) menjadi teks (Draft/Publish).

tambah(): Menampilkan modal form untuk menambahkan data baru.

edit(data): Mengisi modal form dengan data artikel yang akan diubah.

hapus(index, id): Mengirim request DELETE ke API dan memperbarui tampilan.

saveData(): Mengirim request POST (untuk tambah) atau PUT (untuk ubah) ke API dan memperbarui data.

Langkah 5: Menguji Aplikasi Frontend VueJS
Pastikan server CodeIgniter Anda (dari lab7_php_ci) berjalan dan API http://localhost:8080/post dapat diakses.

Buka browser Anda dan akses aplikasi VueJS: http://localhost/lab8_vuejs/index.html (sesuaikan URL dengan lokasi Anda).

Mencoba Menambah Data:

Klik tombol "Tambah Data".

Isi form pada modal dan klik "Simpan".

Data baru akan muncul di tabel.

Mencoba Mengubah Data:

Klik link "Edit" pada salah satu baris artikel.

Modal akan muncul dengan data terisi. Ubah data dan klik "Simpan".

Perubahan akan terlihat di tabel.

![Tabel Data VueJS](Dokumentasi/tabel-data.png)
![Form Tambah Data VueJS](Dokumentasi/form-tambah.png)
![Form Ubah Data VueJS](Dokumentasi/form-edit.png)