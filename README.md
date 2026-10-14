
# SIGAP — WebGIS Tanggap Darurat Kota Semarang

**Sistem Informasi Geospasial Aksesibilitas Layanan Darurat dan Keamanan Masyarakat**

SIGAP merupakan prototipe WebGIS untuk memvisualisasikan fasilitas layanan darurat di Kota Semarang serta mendukung analisis aksesibilitas melalui peta interaktif, pencarian fasilitas terdekat, routing, service area, dan simulasi insiden.

## 1. Tujuan Pengembangan

- Mengintegrasikan informasi fasilitas layanan darurat dalam satu peta interaktif.
- Membantu pengguna menemukan fasilitas berdasarkan lokasi dan kategori.
- Menyajikan estimasi rute dan waktu perjalanan menuju fasilitas.
- Memvisualisasikan jangkauan layanan berdasarkan estimasi waktu tempuh.
- Mendukung simulasi analisis respons terhadap titik insiden.

## 2. Fitur Utama

### Peta Interaktif
Menampilkan peta Kota Semarang beserta lokasi fasilitas dan batas administrasi yang tersedia.

### Filter Fasilitas
Memungkinkan pengguna memilih kategori fasilitas medis, keamanan, kebakaran, dan kebencanaan sesuai data aplikasi.

### Fasilitas Terdekat
Mengidentifikasi fasilitas terdekat dari lokasi pengguna atau titik insiden.

### Routing
Menampilkan rute menuju fasilitas menggunakan layanan routing berbasis jaringan jalan. Waktu perjalanan merupakan estimasi dan tidak selalu mencerminkan kondisi lalu lintas terkini.

### Service Area
Menampilkan perkiraan jangkauan berdasarkan kelas waktu tempuh 5, 10, dan 15 menit. Kelas tersebut merupakan parameter analisis prototipe, bukan standar waktu tanggap resmi.

### Simulasi Insiden
Memungkinkan pengguna menentukan titik kejadian, mengidentifikasi fasilitas medis dan keamanan terdekat, serta menghitung estimasi rute respons.

### Navigasi Lokasi
Menggunakan geolokasi perangkat apabila izin browser diberikan dan perangkat mendukung pembaruan posisi.

## 3. Teknologi

- **HTML** — struktur halaman.
- **CSS** — tampilan, tata letak, dan animasi.
- **JavaScript** — logika aplikasi dan interaksi.
- **Leaflet** — peta interaktif.
- **OpenStreetMap** — peta dasar.
- **GeoJSON dan JSON** — format penyimpanan data fasilitas.
- **Layanan routing eksternal** — perhitungan rute dan estimasi waktu perjalanan.

## 4. Struktur Repository

```text
project-Osig/
├── SIGAP_GitHub_FINAL_v13_6_7/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   ├── fasilitas_semarang.geojson
│   ├── damkar_semarang.json
│   ├── sigap-semarang-intro.png
│   ├── sigap-semarang-rescue-bg.png
│   └── README.md
├── index.html
├── style.css
├── script.js
├── fasilitas_semarang.geojson
├── damkar_semarang.json
├── sigap-semarang-intro.png
├── sigap-semarang-rescue-bg.png
└── README.md
```

Struktur ini menggambarkan file yang terlihat pada repository. Pastikan aplikasi yang dipublikasikan menggunakan file pada lokasi yang benar.

## 5. Fungsi File

| File | Fungsi |
|---|---|
| `index.html` | Menyusun struktur halaman dan komponen antarmuka. |
| `style.css` | Mengatur desain, tata letak, responsivitas, dan animasi. |
| `script.js` | Mengatur peta, marker, pemuatan data, pencarian, routing, dan simulasi. |
| `fasilitas_semarang.geojson` | Menyimpan data spasial fasilitas utama. |
| `damkar_semarang.json` | Menyimpan data pemadam kebakaran. |
| `sigap-semarang-intro.png` | Ilustrasi pembuka jika digunakan oleh halaman. |
| `sigap-semarang-rescue-bg.png` | Ilustrasi latar splash atau onboarding jika digunakan. |

## 6. Cara Menjalankan Secara Lokal

1. Unduh repository melalui menu **Code → Download ZIP**.
2. Ekstrak file ZIP.
3. Buka folder project menggunakan Visual Studio Code.
4. Jalankan `index.html` menggunakan ekstensi Live Server.
5. Izinkan akses lokasi apabila ingin menggunakan fitur geolokasi.

## 7. Publikasi melalui GitHub Pages

1. Buka repository GitHub.
2. Masuk ke **Settings → Pages**.
3. Pilih branch yang digunakan untuk publikasi, misalnya `main`.
4. Pilih folder root (`/`) apabila `index.html` berada di root repository.
5. Simpan pengaturan dan tunggu deployment selesai.
6. Buka URL yang ditampilkan pada halaman GitHub Pages.

Situs SIGAP:
https://arinisetiya879-lang.github.io/sigap-webgis/

## 8. Batasan Sistem

- Akurasi hasil dipengaruhi kelengkapan dan kebaruan data fasilitas.
- Estimasi rute dipengaruhi jaringan jalan, profil perjalanan, dan layanan routing.
- Waktu perjalanan bukan prediksi lalu lintas real-time.
- Simulasi insiden merupakan demonstrasi analitis, bukan sistem dispatch operasional.
- Hasil service area bergantung pada konfigurasi layanan dan jaringan jalan.
- Fitur geolokasi memerlukan izin pengguna.

## 9. Pengembangan Selanjutnya

- Memvalidasi koordinat dan atribut fasilitas berdasarkan sumber resmi.
- Menambahkan informasi sumber data dan tanggal pembaruan.
- Menguji hasil routing dan service area.
- Meningkatkan tampilan pada perangkat seluler.
- Mengembangkan pengelolaan data dinamis untuk penggunaan lebih lanjut.

## 10. Catatan Akademik

SIGAP merupakan prototipe WebGIS untuk visualisasi dan analisis aksesibilitas fasilitas layanan darurat. Hasil analisis perlu diinterpretasikan berdasarkan kualitas data, parameter pemodelan, dan batasan layanan eksternal yang digunakan.

---

**Nama proyek:** SIGAP WebGIS  
**Wilayah kajian:** Kota Semarang, Jawa Tengah  
**Platform:** GitHub Pages

