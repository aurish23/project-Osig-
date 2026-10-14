
# SIGAP WebGIS — Sistem Informasi Geospasial Tanggap Darurat Kota Semarang

> WebGIS untuk visualisasi fasilitas tanggap darurat, analisis aksesibilitas, pencarian fasilitas terdekat, navigasi, perhitungan rute, service area, dan simulasi penanganan insiden di Kota Semarang.

**Nama proyek:** SIGAP — Sistem Informasi Geospasial Tanggap Darurat dan Layanan Keamanan Masyarakat  
**Wilayah kajian:** Kota Semarang, Jawa Tengah, Indonesia  
**Status:** Prototipe WebGIS  
**Frontend:** HTML, CSS, JavaScript  
**Peta interaktif:** Leaflet  
**Peta dasar:** OpenStreetMap  
**Hosting yang direncanakan/digunakan:** GitHub Pages  
**Database yang direncanakan:** Supabase PostgreSQL  

---

## 1. Deskripsi Proyek

SIGAP WebGIS merupakan prototipe sistem informasi geografis berbasis web yang dirancang untuk membantu pengguna mengetahui persebaran fasilitas tanggap darurat serta memahami aksesibilitas menuju fasilitas tersebut di Kota Semarang.

Aplikasi ini mengintegrasikan informasi spasial dengan fitur pencarian fasilitas, penentuan lokasi terdekat, navigasi, analisis area layanan, dan simulasi respons terhadap kejadian darurat. Informasi ditampilkan melalui peta interaktif agar pengguna dapat memahami hubungan antara lokasi kejadian, fasilitas pelayanan, dan jalur yang dapat digunakan untuk mencapai lokasi tujuan.

SIGAP dikembangkan sebagai media pendukung informasi dan simulasi. Aplikasi ini bukan sistem dispatch resmi, bukan layanan ambulans langsung, dan tidak menggantikan layanan darurat pemerintah.

## 2. Tujuan Pengembangan

1. Menampilkan persebaran fasilitas tanggap darurat dalam bentuk peta interaktif.
2. Membantu pengguna menemukan fasilitas berdasarkan kategori dan lokasi.
3. Mendukung analisis aksesibilitas menuju fasilitas pelayanan.
4. Menyediakan estimasi rute dan waktu perjalanan berdasarkan layanan routing yang digunakan.
5. Menampilkan area jangkauan pelayanan berdasarkan parameter waktu perjalanan.
6. Menyimulasikan alur respons terhadap suatu insiden.
7. Menyediakan dasar pengembangan sistem informasi fasilitas berbasis database.
8. Mendukung pengembangan WebGIS yang dapat diakses melalui browser.

## 3. Fitur Utama

### 3.1 Peta Interaktif

Peta digunakan sebagai antarmuka utama untuk menampilkan lokasi pengguna, fasilitas pelayanan, lokasi kejadian, dan rute perjalanan.

Pengguna dapat menggeser peta, memperbesar atau memperkecil tampilan, serta memilih objek yang ditampilkan.

### 3.2 Persebaran Fasilitas

Aplikasi dirancang untuk menampilkan beberapa kelompok fasilitas, antara lain:

- Fasilitas kesehatan atau medis.
- Kepolisian dan layanan keamanan.
- Pemadam kebakaran.
- Fasilitas penanggulangan bencana atau layanan SAR, apabila tersedia dalam dataset.

Ketersediaan kategori dan kelengkapan titik bergantung pada data yang telah dimasukkan ke aplikasi.

### 3.3 Pencarian dan Filter

Fitur pencarian digunakan untuk membantu pengguna menemukan fasilitas berdasarkan nama atau informasi yang tersedia.

Filter kategori membantu membatasi fasilitas yang ditampilkan agar peta lebih mudah dibaca.

### 3.4 Fasilitas Terdekat

Fitur ini membantu mengidentifikasi fasilitas yang memiliki jarak geografis terdekat terhadap lokasi acuan.

Jarak geografis tidak selalu sama dengan jarak perjalanan melalui jalan. Untuk menentukan fasilitas yang paling sesuai secara operasional, jarak rute dan waktu perjalanan juga perlu dipertimbangkan.

### 3.5 Routing dan Estimasi Perjalanan

Fitur routing digunakan untuk menampilkan jalur perjalanan dari titik awal menuju fasilitas tujuan.

Jika aplikasi menyediakan pilihan moda kendaraan, hasil rute dapat digunakan untuk membandingkan estimasi perjalanan sesuai profil kendaraan yang tersedia.

Estimasi waktu perjalanan dipengaruhi oleh jaringan jalan, konfigurasi layanan routing, dan data yang digunakan. Estimasi tersebut tidak otomatis mencerminkan kondisi lalu lintas secara langsung.

### 3.6 Service Area

Service area digunakan untuk menggambarkan area yang secara estimasi dapat dijangkau dalam rentang waktu tertentu, misalnya 5, 10, dan 15 menit.

Analisis ini dapat membantu memahami cakupan pelayanan dan lokasi yang berpotensi memiliki keterbatasan akses.

Hasil service area perlu dibedakan dari radius lingkaran sederhana. Area berbasis jaringan jalan bergantung pada metode analisis dan data routing yang digunakan.

### 3.7 Navigasi Lokasi

Fitur navigasi dapat memanfaatkan lokasi perangkat apabila pengguna memberikan izin akses lokasi.

Informasi posisi tersebut dapat digunakan sebagai titik awal pencarian atau perhitungan rute. Ketelitian lokasi bergantung pada perangkat, sensor, kondisi lingkungan, dan izin browser.

### 3.8 Simulasi Insiden

Simulasi insiden digunakan untuk menggambarkan alur penanganan suatu kejadian pada peta.

Alur simulasi dapat mencakup:

1. Penentuan lokasi kejadian.
2. Identifikasi fasilitas yang relevan.
3. Perhitungan atau penampilan estimasi jarak dan waktu perjalanan.
4. Visualisasi rute menuju lokasi kejadian.
5. Pengakhiran dan pembersihan tampilan simulasi.

Simulasi ini bersifat demonstratif. Aplikasi tidak otomatis menghubungi ambulans, polisi, pemadam kebakaran, atau petugas lapangan.

### 3.9 Splash Screen, Onboarding, dan Audio

Antarmuka awal digunakan untuk memperkenalkan aplikasi kepada pengguna sebelum masuk ke peta utama.

Onboarding menjelaskan tujuan aplikasi secara ringkas. Audio latar, jika diaktifkan oleh implementasi, digunakan sebagai elemen pendukung pengalaman pengguna. Pemutaran audio dapat bergantung pada kebijakan browser dan interaksi pengguna.

---

## 4. Teknologi yang Digunakan

| Teknologi | Fungsi |
|---|---|
| HTML5 | Menyusun struktur halaman aplikasi |
| CSS3 | Mengatur tata letak, warna, tipografi, animasi, dan responsivitas |
| JavaScript | Menjalankan logika, interaksi, pemrosesan data, dan fitur peta |
| Leaflet | Menampilkan peta interaktif dan objek spasial |
| OpenStreetMap | Menyediakan peta dasar |
| GeoJSON | Menyimpan dan menyajikan data spasial berbasis fitur geografis |
| JSON | Menyimpan data terstruktur, termasuk data fasilitas |
| GitHub | Mengelola versi kode dan berkas proyek |
| GitHub Pages | Menyajikan aplikasi statis melalui web |
| Supabase PostgreSQL | Rancangan database untuk penyimpanan dan pengelolaan data terstruktur |

Layanan routing atau geolokasi tambahan hanya tersedia jika telah dikonfigurasi pada kode aplikasi dan layanan terkait dapat diakses.

---

## 5. Struktur Direktori Proyek

Struktur aktual dapat berbeda sesuai versi proyek yang digunakan. Contoh struktur yang disarankan:

```text
SIGAP-WebGIS/
├── index.html
├── style.css
├── script.js
├── fasilitas_semarang.geojson
├── damkar_semarang.json
├── sigap-semarang-intro.png
├── sigap-semarang-rescue-bg.png
├── assets/
├── README.md
└── .nojekyll
```

Keterangan:

- `index.html`: halaman utama dan struktur komponen aplikasi.
- `style.css`: tampilan visual, tata letak, animasi, dan responsivitas.
- `script.js`: logika peta, pemuatan data, interaksi, dan simulasi.
- `fasilitas_semarang.geojson`: data geografis fasilitas dalam format GeoJSON.
- `damkar_semarang.json`: data pemadam kebakaran dalam format JSON, jika digunakan oleh script.
- `sigap-semarang-intro.png`: ilustrasi untuk tampilan pengenalan aplikasi, jika digunakan.
- `sigap-semarang-rescue-bg.png`: ilustrasi latar yang digunakan pada bagian antarmuka terkait, jika digunakan.
- `assets/`: direktori untuk gambar, ikon, atau aset pendukung lainnya.
- `README.md`: dokumentasi proyek.
- `.nojekyll`: berkas yang dapat digunakan untuk menonaktifkan pemrosesan Jekyll pada GitHub Pages.

Nama dan lokasi berkas harus sesuai dengan path yang dirujuk di dalam kode. Jika data berada di direktori lain, path pemanggilan perlu disesuaikan.

---

## 6. Dokumentasi Fungsi Setiap Script

### 6.1 `index.html`

File `index.html` berfungsi sebagai kerangka utama antarmuka SIGAP WebGIS.

Bagian yang umumnya diatur di dalamnya meliputi:

- Struktur halaman pembuka dan onboarding.
- Kontainer peta.
- Panel pencarian dan filter.
- Panel informasi fasilitas.
- Kontrol navigasi dan rute.
- Panel simulasi insiden.
- Pemanggilan file CSS dan JavaScript.
- Elemen antarmuka untuk menampilkan informasi kepada pengguna.

HTML bertanggung jawab atas struktur dan elemen halaman. Perhitungan jarak, pemuatan data, serta pemrosesan rute dilakukan oleh JavaScript atau layanan yang terhubung.

### 6.2 `style.css`

File `style.css` bertanggung jawab atas tampilan visual aplikasi.

Fungsi utamanya meliputi:

- Mengatur warna, tipografi, dan hierarki visual.
- Menentukan tata letak peta dan panel informasi.
- Mengatur tampilan tombol, kolom pencarian, kartu, dan elemen kontrol.
- Menambahkan transisi serta animasi antarmuka.
- Mengatur tampilan splash screen dan onboarding.
- Menyesuaikan antarmuka terhadap ukuran layar.
- Menentukan status visual elemen, misalnya aktif, tersembunyi, atau sedang ditampilkan.

Perubahan pada CSS sebaiknya diuji pada layar desktop dan perangkat seluler untuk memastikan elemen tetap terbaca dan dapat digunakan.

### 6.3 `script.js`

File `script.js` merupakan bagian utama yang menjalankan interaksi dan logika aplikasi.

Fungsi-fungsi di bawah menjelaskan kelompok tanggung jawab yang perlu didokumentasikan. Nama fungsi spesifik harus mengikuti nama yang benar-benar terdapat di versi `script.js` yang digunakan.

#### A. Inisialisasi peta

Tanggung jawab:

- Membuat objek peta Leaflet.
- Menentukan titik tengah dan tingkat zoom awal.
- Menambahkan peta dasar.
- Menyiapkan layer untuk fasilitas, rute, dan objek spasial lainnya.

Bagian ini menjadi dasar bagi seluruh visualisasi spasial.

#### B. Pemuatan data fasilitas

Tanggung jawab:

- Mengambil data dari file GeoJSON atau JSON.
- Membaca atribut fasilitas.
- Memeriksa apakah data berhasil dimuat.
- Menyediakan data untuk ditampilkan pada peta.
- Menangani kegagalan pemuatan agar kesalahan pada satu dataset tidak menghentikan seluruh aplikasi.

Contoh pola pemuatan GeoJSON dari direktori utama:

```javascript
fetch('./fasilitas_semarang.geojson', {
  cache: 'no-store'
})
  .then(response => {
    if (!response.ok) {
      throw new Error('Data fasilitas gagal dimuat');
    }

    return response.json();
  })
  .then(data => {
    console.log('Data fasilitas berhasil dimuat', data);
  })
  .catch(error => {
    console.error('Kesalahan pemuatan fasilitas:', error);
  });
```

Contoh tersebut merupakan pola umum. Integrasikan ke fungsi pemuatan data yang sudah ada agar tidak terjadi pemanggilan ganda.

#### C. Pengolahan dan penampilan marker

Tanggung jawab:

- Mengubah koordinat fasilitas menjadi marker pada peta.
- Menggunakan ikon sesuai kategori jika tersedia.
- Menampilkan nama dan informasi fasilitas.
- Menghubungkan marker dengan popup atau panel detail.
- Mengelola layer agar fasilitas dapat ditampilkan atau disembunyikan.

Marker harus menggunakan koordinat yang benar dan format data yang sesuai.

#### D. Pencarian dan filter fasilitas

Tanggung jawab:

- Membaca masukan pengguna.
- Mencocokkan kata kunci dengan atribut fasilitas.
- Menyaring data berdasarkan kategori.
- Memperbarui tampilan marker sesuai hasil pencarian.
- Menampilkan informasi ketika tidak ada hasil yang sesuai.

#### E. Perhitungan jarak

Jika digunakan, perhitungan jarak geografis dapat menggunakan rumus Haversine untuk memperkirakan jarak permukaan antara dua koordinat.

Rumus:

\[
a = \sin^2\left(\frac{\Delta\varphi}{2}\right)
+ \cos(\varphi_1)\cos(\varphi_2)
\sin^2\left(\frac{\Delta\lambda}{2}\right)
\]

\[
d = 2R\arcsin(\sqrt{a})
\]

Keterangan:

- \(d\): jarak geografis.
- \(R\): jari-jari rata-rata bumi.
- \(\varphi_1,\varphi_2\): lintang dua titik dalam radian.
- \(\lambda_1,\lambda_2\): bujur dua titik dalam radian.
- \(\Delta\varphi\): selisih lintang.
- \(\Delta\lambda\): selisih bujur.

Hasil Haversine merupakan jarak geografis garis besar, bukan jarak tempuh melalui jaringan jalan.

#### F. Penentuan fasilitas terdekat

Tanggung jawab:

- Menentukan titik acuan.
- Menghitung jarak dari titik acuan ke setiap fasilitas yang relevan.
- Mengurutkan fasilitas berdasarkan jarak.
- Menampilkan fasilitas dengan jarak terkecil.

Jika tujuannya adalah memilih fasilitas dengan waktu respons tercepat, hasil perlu mempertimbangkan jaringan jalan, kondisi akses, dan estimasi waktu perjalanan.

#### G. Routing

Tanggung jawab:

- Menentukan titik awal dan tujuan.
- Mengirim permintaan rute ke layanan routing jika dikonfigurasi.
- Mengolah respons layanan.
- Menampilkan jalur perjalanan pada peta.
- Menampilkan jarak dan estimasi waktu.
- Mengelola kegagalan permintaan atau rute yang tidak tersedia.

Routing memerlukan koneksi ke layanan terkait. Hasil tidak boleh dianggap sebagai informasi lalu lintas langsung kecuali layanan tersebut memang menyediakan dan aplikasi menggunakan data tersebut.

#### H. Service area

Tanggung jawab:

- Mengambil fasilitas atau titik awal analisis.
- Menggunakan parameter jangkauan tertentu.
- Menampilkan area yang dapat dijangkau berdasarkan metode analisis yang digunakan.
- Memperbarui tampilan ketika parameter berubah.

Jika implementasi menggunakan jaringan jalan, kualitas hasil dipengaruhi oleh data jalan dan layanan routing. Jika hanya menggunakan radius geometris, tampilannya tidak dapat dianggap sebagai cakupan jaringan jalan.

#### I. Navigasi dan geolokasi

Tanggung jawab:

- Meminta izin lokasi dari browser.
- Membaca posisi perangkat ketika tersedia.
- Memperbarui posisi pengguna jika fitur tersebut diimplementasikan.
- Menggunakan lokasi sebagai titik awal navigasi.
- Menangani izin ditolak, perangkat tidak mendukung, atau lokasi gagal ditemukan.

Geolokasi browser memerlukan koneksi aman, seperti HTTPS, atau lingkungan lokal yang diizinkan browser.

#### J. Simulasi insiden

Tanggung jawab:

- Menentukan atau menerima koordinat kejadian.
- Menampilkan marker insiden.
- Mencari fasilitas relevan.
- Menampilkan rute atau estimasi perjalanan.
- Menampilkan ringkasan simulasi.
- Membersihkan marker dan rute ketika simulasi diakhiri.

Fungsi penutupan panel dan fungsi pengakhiran simulasi perlu dibedakan. Menutup panel tidak selalu berarti semua layer simulasi telah dihapus, sehingga keduanya perlu diuji.

#### K. Splash screen dan onboarding

Tanggung jawab:

- Mengatur tampilan pembuka.
- Menampilkan pengenalan singkat.
- Mengelola perpindahan ke halaman utama.
- Menyembunyikan elemen pengantar setelah pengguna melanjutkan.

#### L. Audio latar

Jika audio latar dibuat menggunakan Web Audio API atau metode browser lainnya, tanggung jawab bagian ini dapat mencakup:

- Membuat sumber suara.
- Mengatur parameter audio.
- Mengaktifkan atau menghentikan pemutaran.
- Menangani batasan autoplay browser.
- Membersihkan sumber audio ketika tidak lagi dibutuhkan.

Fungsi ini hanya berlaku jika kode audio memang terdapat pada versi aplikasi yang digunakan.

#### M. Penanganan kesalahan

Bagian penanganan kesalahan sebaiknya mengelola:

- Dataset yang tidak dapat diakses.
- Respons layanan routing yang gagal.
- Koordinat tidak valid.
- Izin lokasi ditolak.
- Elemen HTML yang tidak ditemukan.
- Kegagalan koneksi ke database, jika integrasi Supabase telah diterapkan.

Pesan kesalahan sebaiknya mudah dipahami pengguna. Informasi teknis lengkap dapat dicatat melalui console browser untuk membantu proses debugging.

---

## 7. Format Data Spasial

### 7.1 GeoJSON

GeoJSON digunakan untuk menyimpan objek geografis beserta atributnya.

Contoh struktur titik fasilitas:

```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "nama": "Contoh Fasilitas",
        "kategori": "medis",
        "alamat": "Kota Semarang"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [
          110.4203,
          -6.9932
        ]
      }
    }
  ]
}
```

Pada GeoJSON, urutan koordinat titik adalah:

1. Bujur atau longitude.
2. Lintang atau latitude.

Koordinat contoh di atas hanya untuk ilustrasi struktur dan harus diverifikasi sebelum digunakan sebagai lokasi fasilitas sebenarnya.

### 7.2 JSON

JSON dapat digunakan untuk menyimpan data fasilitas terstruktur yang belum disusun dalam format GeoJSON.

Contoh atribut yang dapat digunakan:

- Identitas fasilitas.
- Nama fasilitas.
- Kategori.
- Alamat.
- Latitude.
- Longitude.
- Nomor kontak, jika tersedia dan layak dipublikasikan.
- Sumber data.
- Tanggal pembaruan.

Atribut yang tersedia harus disesuaikan dengan dataset aktual. Dokumentasi tidak menjamin semua atribut tersebut sudah terdapat di dalam file proyek.

---

## 8. Menjalankan Aplikasi Secara Lokal

SIGAP merupakan aplikasi frontend statis. Jika file HTML, CSS, JavaScript, dan dataset tersedia, aplikasi dapat dijalankan melalui server lokal sederhana.

### Langkah 1 — Siapkan berkas

Pastikan `index.html`, `style.css`, `script.js`, dan seluruh dataset berada di lokasi yang sesuai dengan path di kode.

### Langkah 2 — Buka folder proyek

Buka folder proyek menggunakan Visual Studio Code.

### Langkah 3 — Jalankan server lokal

Salah satu cara adalah menggunakan ekstensi Live Server pada Visual Studio Code.

1. Instal ekstensi Live Server jika belum tersedia.
2. Buka `index.html`.
3. Pilih **Open with Live Server**.
4. Buka alamat lokal yang ditampilkan browser.

Alternatifnya, jika Python tersedia, jalankan perintah berikut dari direktori proyek:

```bash
python -m http.server 8000
```

Kemudian buka:

```text
http://localhost:8000
```

Server lokal membantu menguji pemanggilan file dan dataset melalui HTTP. Membuka `index.html` langsung melalui `file://` dapat menyebabkan masalah pada permintaan `fetch()`.

---

## 9. Hosting Menggunakan GitHub Pages

GitHub Pages dapat digunakan untuk menyajikan aplikasi statis yang terdiri atas HTML, CSS, JavaScript, dan berkas data.

### Langkah 1 — Unggah berkas

Pastikan seluruh file yang dibutuhkan tersedia di repositori.

### Langkah 2 — Periksa lokasi file

Jika `index.html` berada di direktori utama, path aset dan dataset harus merujuk pada lokasi yang sesuai.

Contoh:

```javascript
fetch('./fasilitas_semarang.geojson');
```

Jika file berada di subdirektori, path harus disesuaikan dengan struktur tersebut.

### Langkah 3 — Aktifkan GitHub Pages

1. Buka repositori GitHub.
2. Masuk ke **Settings**.
3. Pilih **Pages**.
4. Tentukan sumber deployment sesuai struktur repositori.
5. Simpan pengaturan dan tunggu proses deployment.

### Langkah 4 — Uji hasil deployment

Periksa:

- Halaman utama dapat dibuka.
- Peta dasar muncul.
- Marker fasilitas ditampilkan.
- Dataset berhasil dimuat.
- Gambar dan ikon tidak rusak.
- Pencarian dan filter berfungsi.
- Routing serta simulasi dapat dijalankan.
- Tidak ada kesalahan kritis pada console browser.

GitHub Pages hanya menyediakan hosting frontend statis. GitHub Pages tidak menjalankan server backend sendiri dan tidak menyediakan database relasional untuk aplikasi.

---

## 10. Rancangan Integrasi Database Supabase

### 10.1 Tujuan Integrasi

Supabase direncanakan sebagai database untuk menyimpan dan mengelola informasi fasilitas tanggap darurat.

Dengan integrasi ini, data fasilitas dapat dikelola melalui database sehingga pembaruan data tidak selalu harus dilakukan dengan mengganti file JSON atau GeoJSON secara manual.

Integrasi database perlu diterapkan pada kode aplikasi sebelum fitur ini dapat digunakan.

### 10.2 Arsitektur yang Direncanakan

```text
Pengguna
   |
   v
Frontend SIGAP
(HTML, CSS, JavaScript)
   |
   v
Supabase Client
   |
   v
Supabase PostgreSQL
   |
   v
Data fasilitas dan informasi terkait
```

Frontend mengambil data melalui API Supabase menggunakan konfigurasi dan hak akses yang sesuai.

### 10.3 Rancangan Tabel `facilities`

Tabel ini dapat menyimpan informasi fasilitas yang akan ditampilkan pada peta.

| Kolom | Tipe | Keterangan |
|---|---|---|
| id | bigint | Identitas fasilitas |
| name | text | Nama fasilitas |
| category | text | Kategori fasilitas |
| address | text | Alamat |
| latitude | double precision | Lintang |
| longitude | double precision | Bujur |
| phone | text | Nomor kontak jika tersedia |
| source | text | Sumber data |
| updated_at | timestamptz | Waktu pembaruan |

### 10.4 Contoh SQL Pembuatan Tabel

Jalankan SQL berikut di SQL Editor proyek Supabase setelah meninjau struktur data yang dibutuhkan.

```sql
create table public.facilities (
  id bigint generated by default as identity primary key,
  name text not null,
  category text not null,
  address text,
  latitude double precision not null,
  longitude double precision not null,
  phone text,
  source text,
  updated_at timestamptz not null default now(),

  constraint facilities_latitude_valid
    check (latitude >= -90 and latitude <= 90),

  constraint facilities_longitude_valid
    check (longitude >= -180 and longitude <= 180)
);

create index facilities_category_idx
  on public.facilities(category);
```

SQL tersebut merupakan contoh awal skema database. Skema perlu disesuaikan jika dataset memiliki identitas unik, struktur kategori, atau kebutuhan relasi tambahan.

### 10.5 Keamanan Database

Supabase mendukung Row Level Security (RLS) untuk mengatur data yang dapat dibaca atau diubah oleh setiap jenis pengguna.

Sebelum menghubungkan frontend, tentukan kebutuhan akses:

- Apakah semua pengguna boleh membaca data fasilitas?
- Siapa yang berhak menambah fasilitas?
- Siapa yang berhak mengubah koordinat?
- Siapa yang berhak menghapus fasilitas?
- Apakah perubahan data membutuhkan autentikasi?

Untuk data fasilitas publik, kebijakan akses baca dapat dibuat terbuka jika memang sesuai kebutuhan. Hak tulis sebaiknya dibatasi kepada pengguna atau peran yang berwenang.

Mengaktifkan RLS saja tidak otomatis membuat tabel dapat dibaca atau ditulis oleh pengguna. Kebijakan, grant, dan konfigurasi akses harus disesuaikan.

Jangan menempatkan secret key atau `service_role` key di dalam JavaScript frontend. Gunakan publishable key dengan kebijakan akses yang tepat.

### 10.6 Contoh Koneksi Supabase dari JavaScript

Contoh berikut merupakan pola integrasi dasar, bukan bukti bahwa SIGAP telah terhubung ke database.

```javascript
import { createClient } from
  'https://cdn.jsdelivr.net/npm/@supabase/supabase-js/+esm';

const SUPABASE_URL =
  'https://PROJECT_ID.supabase.co';

const SUPABASE_PUBLISHABLE_KEY =
  'YOUR_SUPABASE_PUBLISHABLE_KEY';

const supabase = createClient(
  SUPABASE_URL,
  SUPABASE_PUBLISHABLE_KEY
);

async function loadFacilities() {
  const { data, error } = await supabase
    .from('facilities')
    .select('*');

  if (error) {
    console.error(
      'Gagal mengambil data fasilitas:',
      error.message
    );

    return [];
  }

  return data ?? [];
}
```

Sebelum menggunakan contoh ini:

1. Buat proyek Supabase.
2. Buat tabel `facilities`.
3. Atur RLS, kebijakan akses, dan izin yang dibutuhkan.
4. Isi URL proyek dan publishable key yang benar.
5. Pastikan pemuatan data dilakukan dari script yang sesuai.
6. Ubah data yang diterima menjadi marker Leaflet.
7. Uji pembacaan data dan penanganan kesalahan.

Jika memakai sintaks `import`, file JavaScript harus dimuat sebagai modul, misalnya menggunakan atribut `type="module"` pada elemen script. Sesuaikan dengan struktur `index.html` yang digunakan.

### 10.7 Rencana Migrasi Data

Tahapan yang disarankan:

1. Memeriksa dan membersihkan data JSON atau GeoJSON.
2. Menentukan kolom database berdasarkan atribut yang tersedia.
3. Mengimpor data fasilitas ke Supabase.
4. Memverifikasi jumlah data dan koordinat.
5. Mengatur kebijakan akses database.
6. Menghubungkan frontend ke Supabase.
7. Mengubah fungsi pemuatan data agar mengambil data dari database.
8. Menghubungkan hasil query dengan proses pembuatan marker.
9. Menguji seluruh fitur yang menggunakan data fasilitas.
10. Menyusun prosedur pembaruan dan pencadangan data.

---

## 11. Pengembangan Database Lanjutan

Setelah tabel fasilitas berjalan, database dapat dikembangkan dengan tabel tambahan sesuai kebutuhan.

### 11.1 Tabel `incident_reports`

Tabel ini dapat digunakan jika aplikasi kelak memerlukan pencatatan laporan kejadian secara persisten.

Contoh atribut yang dapat dipertimbangkan:

- `id`
- `incident_type`
- `latitude`
- `longitude`
- `description`
- `status`
- `created_at`

Simpan data lokasi kejadian hanya sesuai kebutuhan dan dengan memperhatikan privasi. Hindari menyimpan identitas pribadi yang tidak diperlukan.

### 11.2 Tabel `facility_updates`

Tabel ini dapat digunakan untuk mencatat perubahan informasi fasilitas, misalnya perubahan alamat, koordinat, atau status operasional.

### 11.3 Autentikasi Pengelola

Supabase Auth dapat dipertimbangkan untuk membatasi akses pengelolaan data kepada pengguna yang berwenang.

Fitur ini memerlukan konfigurasi autentikasi, kebijakan database, dan antarmuka pengelolaan tersendiri.

---

## 12. Pengujian dan Validasi

Pengujian perlu dilakukan pada aspek berikut.

### A. Data spasial

- Koordinat berada pada rentang yang valid.
- Urutan longitude dan latitude sesuai format.
- Tidak ada fasilitas duplikat yang tidak disengaja.
- Nama dan kategori fasilitas konsisten.
- Sumber dan tanggal pembaruan dapat ditelusuri.

### B. Fungsionalitas

- Peta tampil dengan baik.
- Pencarian dan filter menghasilkan keluaran yang sesuai.
- Marker dan panel informasi merujuk pada fasilitas yang benar.
- Fitur terdekat menggunakan titik acuan yang benar.
- Rute ditampilkan ketika layanan routing berhasil.
- Panel simulasi dapat dibuka dan ditutup.
- Tombol pengakhiran simulasi membersihkan elemen yang relevan.
- Penolakan izin lokasi tidak membuat aplikasi berhenti.
- Kegagalan pemuatan data ditangani dengan baik.

### C. Deployment

- Semua aset dapat diakses dari alamat GitHub Pages.
- Tidak ada path lokal yang tertinggal.
- Nama file sesuai dengan yang dipanggil di kode.
- Tidak ada kredensial rahasia pada file publik.
- Tidak ada kesalahan JavaScript yang menghambat fitur utama.

### D. Validasi operasional

Informasi fasilitas, nomor kontak, dan status layanan harus diverifikasi dengan sumber yang dapat dipercaya. Estimasi rute dan simulasi tidak boleh diperlakukan sebagai konfirmasi bahwa petugas telah menerima atau menjalankan penanganan insiden.

---

## 13. Permasalahan Umum

### Peta tidak muncul

Periksa koneksi internet, pemanggilan Leaflet, elemen kontainer peta, serta pengaturan tinggi dan lebar kontainer.

### Marker tidak muncul

Periksa:

- Apakah file data berhasil dimuat.
- Apakah format JSON atau GeoJSON valid.
- Apakah koordinat benar.
- Apakah kode membaca struktur data yang sesuai.
- Apakah ada kesalahan pada console browser.

### Data gagal dimuat di GitHub Pages

Pastikan nama file, huruf besar-kecil, dan path sesuai. Periksa juga apakah file berada di direktori utama atau subdirektori.

### Gambar atau ikon tidak muncul

Pastikan file benar-benar tersedia di repositori dan path relatifnya sesuai dengan struktur deployment.

### Routing tidak berhasil

Periksa koneksi internet, konfigurasi layanan routing, format koordinat, batas permintaan layanan, dan respons error.

### Lokasi pengguna tidak ditemukan

Pastikan browser memberi izin lokasi, perangkat mendukung geolokasi, dan halaman dibuka melalui HTTPS atau lingkungan lokal yang sesuai.

### Supabase mengembalikan error

Periksa URL proyek, publishable key, nama tabel, struktur kolom, RLS, kebijakan akses, dan hak akses query.

---

## 14. Batasan Sistem

1. SIGAP masih merupakan prototipe WebGIS.
2. Kelengkapan dan ketepatan informasi bergantung pada dataset yang tersedia.
3. Estimasi jarak geografis berbeda dari jarak tempuh melalui jalan.
4. Estimasi waktu perjalanan tidak selalu mewakili kondisi lalu lintas saat ini.
5. Simulasi insiden tidak sama dengan proses dispatch layanan darurat yang sesungguhnya.
6. Geolokasi bergantung pada perangkat dan izin pengguna.
7. Supabase baru berfungsi setelah integrasi database diterapkan dan diuji.
8. Kualitas analisis service area bergantung pada metode, data jalan, dan layanan yang digunakan.
9. Informasi fasilitas perlu diperbarui dan diverifikasi secara berkala.

---

## 15. Rencana Pengembangan

Pengembangan selanjutnya dapat mencakup:

- Integrasi Supabase untuk pengelolaan data fasilitas.
- Panel admin untuk memperbarui data.
- Autentikasi pengguna yang berwenang.
- Pencatatan dan visualisasi laporan kejadian.
- Validasi data dan riwayat pembaruan fasilitas.
- Penyempurnaan analisis aksesibilitas.
- Perbandingan jarak, waktu, dan alternatif rute.
- Peningkatan tampilan responsif.
- Pengujian kegunaan pada perangkat desktop dan seluler.
- Dokumentasi sumber data dan metode analisis.

---

## 16. Referensi Dokumentasi

- Leaflet: https://leafletjs.com/reference.html
- OpenStreetMap: https://www.openstreetmap.org/
- GeoJSON: https://geojson.org/
- GitHub Pages: https://docs.github.com/en/pages
- Supabase JavaScript: https://supabase.com/docs/reference/javascript/introduction
- Supabase Database: https://supabase.com/docs/guides/database/overview
- Supabase Row Level Security: https://supabase.com/docs/guides/database/postgres/row-level-security
- Supabase Secure Data: https://supabase.com/docs/guides/database/secure-data

---

## 17. Penutup

SIGAP WebGIS dikembangkan sebagai prototipe sistem informasi geospasial untuk membantu visualisasi fasilitas tanggap darurat dan analisis aksesibilitas di Kota Semarang. Integrasi peta interaktif, pencarian fasilitas, routing, service area, dan simulasi insiden diharapkan dapat mendukung pemahaman spasial terhadap kebutuhan pelayanan darurat.

Pengembangan lebih lanjut memerlukan validasi data, pengujian fungsionalitas, dokumentasi metode analisis, serta implementasi database yang aman. Informasi yang ditampilkan perlu dipahami sebagai dukungan informasi dan simulasi, bukan pengganti layanan darurat resmi.

**SIGAP — Tanggap Bersama, Masyarakat Lebih Aman.**
