# Wajah Jawa Timur dalam Angka dan Cerita

Data storytelling interaktif yang memotret ketimpangan pembangunan di **38 kabupaten/kota Provinsi Jawa Timur** menggunakan data Badan Pusat Statistik (BPS). Halaman ini memotret Jawa Timur dari tiga sisi: **di mana** kemiskinan dan kualitas hidup tersebar (kemiskinan, IPM, dan sanitasi per kabupaten/kota), **bagaimana** wilayah-wilayah itu saling mirip dan berkaitan (PCA, k-means, dan korelasi), dan **untuk apa** penduduk membelanjakan penghasilannya (pengeluaran per kapita). Bentuknya satu situs statis bergaya *scrollytelling*: globe 3D, grafik interaktif, dan narasi yang berjalan dari slide ke slide, lengkap dengan musik latar dan video.

|||
|-|-|
|**Aplikasi (publik)**|https://kemiskinan-dan-ketimpangan-di-jawa-timur.vercel.app/|
|**Repositori**|[github.com/AnisaGiriRamadhani/3SD1\_222312984\_ANISA-GIRI-RAMADHANI](https://github.com/AnisaGiriRamadhani/3SD1_222312984_ANISA-GIRI-RAMADHANI)|
|**Penulis**|Anisa Giri Ramadhani, NIM 222312984, Kelas 3SD1|
|**Program studi**|D-IV Komputasi Statistik, Politeknik Statistika STIS|
|**Sumber data utama**|BPS (Badan Pusat Statistik)|

> Satu provinsi, dua wajah: pusat metropolitan yang melaju pesat, dan wilayah penyangga serta kepulauan yang masih butuh percepatan layanan dasar.

## Tiga Topik Visualisasi

|Topik|Pertanyaan|Teknik|Data BPS|
|-|-|-|-|
|Geospasial|Wilayah mana yang paling rentan dan mana yang unggul dalam kemiskinan, kedalaman kemiskinan, sanitasi, dan IPM?|Globe 3D dengan menara data per kab/kota (tinggi dan warna mengikuti nilai indikator) dan peta simbol proporsional (lingkaran)|Persentase penduduk miskin, P1, sanitasi layak, dan IPM per kab/kota, 2024|
|Multivariat|Wilayah mana yang mirip satu sama lain, dan indikator apa yang saling berkaitan?|Peta kemiripan PCA, klaster k-means, radar profil kelompok, heatmap korelasi, dan sebar IPM vs kemiskinan dengan garis regresi|Seluruh indikator kemiskinan, IPM (beserta komponennya), dan layanan dasar per kab/kota, 2024|
|Komposisi berhierarki|Untuk apa uang dibelanjakan?|Sunburst dan treemap pengeluaran per kapita (kelompok makanan dan non-makanan, lalu komoditas)|Rata-rata pengeluaran per kapita sebulan menurut kelompok komoditas, Jawa Timur (Susenas), 2024|

Selain tiga topik itu, ada slide **"Sekilas dari 38 wilayah"** (enam angka kunci) dan slide **"Jelajahi sendiri"** untuk memilih indikator dan membandingkan wilayah secara bebas.

### Alur 15 slide

|#|Bagian|Isi|
|-|-|-|
|1–2|Sampul \& pengantar|Gambaran umum 38 kabupaten/kota|
|3–6|Globe 3D|Menara data untuk persentase penduduk miskin, kedalaman kemiskinan (P1), akses sanitasi layak, dan IPM|
|7|Sekilas|Enam angka kunci dengan video latar|
|8|Simbol proporsional|Lingkaran berukuran sesuai persentase penduduk miskin|
|9|IPM vs kemiskinan|Sebar dengan garis regresi|
|10|PCA|Peta kemiripan wilayah dan klaster|
|11|Profil kelompok|Radar rata-rata ternormalisasi per kelompok|
|12|Korelasi|Heatmap korelasi antarindikator|
|13|Pengeluaran|Sunburst dan treemap|
|14|Jelajahi sendiri|Pilih indikator, klik wilayah di globe atau daftar peringkat|
|15|Penutup|Kesimpulan dan implikasi kebijakan|

## Fitur yang Dipenuhi

**Geospasial**

* Tingkat kabupaten/kota (38 wilayah), dengan dua jenis tampilan: globe 3D dan peta simbol proporsional.
* Indikator berupa persentase dan indeks (persentase miskin, sanitasi, IPM, P1).
* Legenda skala warna, tooltip, zoom (+/−, penggeser, dan *scroll*), putar globe, dan klik wilayah untuk melihat nama dan nilainya.
* Daftar peringkat wilayah yang tersinkron dengan pilihan di globe.

**Multivariat**

* PCA dua komponen dengan klaster k-means (3 kelompok: kerentanan tinggi, menengah, rendah).
* Pemilihan wilayah pada grafik tersinkron ke grafik lain.
* Radar, heatmap korelasi (skala biru–merah), dan regresi sederhana IPM terhadap kemiskinan.

**Komposisi berhierarki**

* Hierarki: total, kelompok (makanan dan non-makanan), lalu komoditas.
* Dua representasi berbeda yang bisa dialihkan lewat tab: sunburst dan treemap.

**Ketentuan umum**

* Interaksi: pilihan indikator, tooltip, zoom, klik wilayah, tombol *reset*, dan putar ulang cerita ("Mulai lagi").
* Warna klaster memakai palet Okabe-Ito (oranye-merah, kuning-oranye, dan biru).
* Responsif: ada navigasi sentuh untuk ponsel, dan tema gelap/terang mengikuti pengaturan perangkat.
* Sumber: setiap grafik mencantumkan "Sumber: BPS Statistics", dan slide penutup mencantumkan sumber olahan.

## Sumber Data

Tanggal akses: **4 Oktober 2026**

|Data|Judul tabel/publikasi|Tahun|URL|
|-|-|-|-|
|Penduduk miskin|Presentase Penduduk Miskin (P0) Menurut Kabupaten/Kota|2024|https://www.bps.go.id/id/query-builder|
|Garis kemiskinan|Garis Kemiskinan Menurut Kabupaten/Kota|2024|https://www.bps.go.id/id/query-builder|
|Kedalaman kemiskinan (P1)|Indeks Kedalaman Kemiskinan (P1) Menurut Kabupaten/Kota|2024|https://www.bps.go.id/id/query-builder|
|Keparahan kemiskinan (P2)|Indeks Keparahan Kemiskinan (p2) Menurut Kabupaten/Kota|2024|https://www.bps.go.id/id/query-builder|
|IPM|\[Metode Baru] Indeks Pembangunan Manusia (IPM) |2024|https://www.bps.go.id/id/query-builder|
|Angka harapan hidup (UHH)|Angka Harapan Hidup Menurut Kabupaten/Kota dan Jenis Kelamin|2024|https://www.bps.go.id/id/query-builder|
|Harapan lama sekolah (HLS)|\[Metode Baru] Harapan Lama Sekolah|2024|https://www.bps.go.id/id/query-builder|
|Rata-rata lama sekolah (RLS)|\[Metode Baru] Rata-Rata Lama Sekolah Jawa Timur|2024|https://www.bps.go.id/id/query-builder|
|Pengeluaran per kapita (komponen IPM)|\[Metode Baru] Pengeluaran Per Kapita Disesuaikan|2024|https://www.bps.go.id/id/query-builder|
|Sanitasi layak|Presentase Ruta Yang Memiliki Akses Terhadap Sanitasi Layak Menurut Kabupaten/Kota|2024|https://www.bps.go.id/id/query-builder|
|Air minum layak|Presentase Ruta Yang Memiliki Akses Terhadap Sumber Air Menurut Kabupaten/Kota|2024|https://www.bps.go.id/id/query-builder|
|Pengeluaran per kapita menurut komoditas (Susenas)|Rata-rata Pengeluaran per Kapita Sebulan Provinsi Jawa Timur menurut Kelompok Komoditas dan Klasifikasi Desa (Rupiah), September 2024|2024|https://www.bps.go.id/id/publication/2025/05/28/b67b4702334f3123221372ba/pengeluaran-untuk-konsumsi-penduduk-indonesia--september-2024.html|
|Garis daratan dunia (non-BPS)|datasets/geo-countries (GeoJSON, dimuat saat halaman dibuka)|–|https://github.com/datasets/geo-countries|

## Pengolahan Data

Semua pengolahan dilakukan di dalam `index.html` sehingga dapat direproduksi.

* **Data:** 11 berkas indikator per kab/kota digabung menjadi satu tabel (38 baris, kunci kode wilayah), sedangkan berkas pengeluaran per komoditas menjadi tabel tersendiri. Keduanya disimpan sebagai CSV di dalam skrip `index.html`, lalu dibaca saat halaman dimuat.
* **Normalisasi:** setiap indikator diubah ke z-score sebelum dianalisis.
* **PCA:** dua komponen utama dihitung dari matriks korelasi dengan *power iteration*; proporsi varians yang dijelaskan ditampilkan pada grafik.
* **Klaster:** k-means dengan 3 kelompok pada ruang indikator ternormalisasi, diberi label kerentanan tinggi, menengah, dan rendah.
* **Korelasi dan regresi:** korelasi Pearson antarindikator, serta regresi linear sederhana IPM terhadap persentase penduduk miskin.
* **Pengeluaran:** nilai per komoditas dikelompokkan menjadi makanan dan non-makanan, lalu dirender sebagai sunburst dan treemap.
* **Kalimat temuan** (peringkat tertinggi/terendah, selisih, rasio) dihitung otomatis dari data, bukan diketik manual.

## Cara Menjalankan Secara Lokal

Tidak perlu proses *build* maupun instalasi dependensi. Layani folder ini dengan server statis apa pun:

```bash
git clone https://github.com/AnisaGiriRamadhani/3SD1\_222312984\_ANISA-GIRI-RAMADHANI.git
cd 3SD1\_222312984\_ANISA-GIRI-RAMADHANI

# Python
python3 -m http.server 8000

# atau Node.js
npx serve .
```

Aplikasi terbuka di `http://localhost:8000`. Membuka `index.html` langsung dari berkas (`file://`) umumnya tetap bisa, tetapi sebagian peramban membatasi pemuatan media, jadi server lokal lebih disarankan. Halaman memerlukan koneksi internet untuk memuat pustaka dari CDN.

**Kontrol:** gulir atau gunakan tombol ▲ ▼ untuk berpindah slide. Seret globe untuk memutar, gunakan tombol `+`/`−` atau penggeser untuk zoom, dan klik tombol speaker untuk menyalakan musik (peramban memblokir pemutaran otomatis dengan suara).

## Struktur Repositori

```
.
├── index.html              # seluruh aplikasi (HTML, CSS, JS, dan data)
├── vercel.json             # konfigurasi deploy Vercel
├── Data/                   # 12 berkas Excel BPS (lihat bagian Sumber Data)
├── musik-latar.mp3         # musik latar (tombol suara di kiri atas)
├── video-sekilas.mp4       # video latar slide "Sekilas dari 38 wilayah"
├── image-penutup.jpg       # foto slide penutup
├── latar-bab.jpg           # latar slide simbol proporsional
├── latar-simpang-lima.jpg  # latar slide IPM vs kemiskinan
├── latar-bimasakti.jpg     # latar slide PCA
├── latar-api-biru.jpg      # latar slide profil kelompok
├── latar-api-biru-2.jpg    # latar slide korelasi
└── latar-bintang-ranu.jpg  # latar slide pengeluaran
```

> `index.html` memanggil berkas gambar di atas \*\*dengan nama persis seperti tertulis\*\*. Foto sampul (Gunung Bromo) dan foto pengantar (Monumen Suro dan Boyo) sudah tertanam di dalam HTML, jadi tidak perlu berkas terpisah.

## Deployment

Dideploy sebagai situs statis di Vercel. Tidak ada *build command*; `vercel.json` mengaktifkan `cleanUrls` dan mengarahkan semua rute ke `index.html`:

```json
{
  "version": 2,
  "cleanUrls": true,
  "rewrites": \[{ "source": "/(.\*)", "destination": "/index.html" }]
}
```

Untuk deploy sendiri: impor repositori ke [Vercel](https://vercel.com) dengan preset **Other**, atau jalankan `npx vercel --prod` dari folder proyek. Berkas statis yang ada (musik, video, gambar) disajikan lebih dulu sebelum aturan *rewrite* diterapkan, sehingga tetap termuat normal.

### Dependensi eksternal (CDN)

|Pustaka / layanan|Kegunaan|
|-|-|
|[three.js 0.128.0](https://threejs.org)|Globe 3D dan menara data|
|[Plotly.js 2.35.2](https://plotly.com/javascript/)|Grafik interaktif (scatter, radar, heatmap, sunburst, treemap)|
|Google Fonts (Fraunces, Plus Jakarta Sans, Instrument Serif, Newsreader, Great Vibes)|Tipografi|
|[datasets/geo-countries](https://github.com/datasets/geo-countries)|Garis daratan dunia pada globe|

Jika GeoJSON dunia gagal dimuat, konteks daratan di globe tidak tampil, tetapi bagian lain tetap berjalan.

## Keterbatasan

* Data bersifat *cross-section* satu tahun (2024), sehingga tidak menunjukkan tren antartahun.
* PCA dan k-means bersifat eksploratif: jumlah klaster (3) ditetapkan di awal, dan hasil klaster bergantung pada indikator yang dipilih.
* Regresi IPM terhadap kemiskinan menunjukkan asosiasi, bukan hubungan sebab-akibat.
* Data pengeluaran per kapita hanya tersedia di tingkat provinsi, bukan per kabupaten/kota.
* Membutuhkan peramban dengan dukungan WebGL dan koneksi internet (CDN).

## Deklarasi Penggunaan AI

\[Sesuaikan bagian ini dengan penggunaan alat bantu AI yang sebenarnya, misalnya untuk menyusun kode atau draf dokumentasi. Seluruh isi proyek, termasuk pemilihan data, rancangan visualisasi, dan interpretasi, menjadi tanggung jawab penulis.]

## Lisensi dan Atribusi

Data statistik bersumber dari Badan Pusat Statistik (BPS). Foto, video, dan musik latar mengikuti hak cipta masing-masing pemilik; pastikan hak pakainya sebelum dipublikasikan secara luas. Proyek ini dibuat untuk keperluan akademik.

