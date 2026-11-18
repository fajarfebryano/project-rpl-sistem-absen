# project-rpl-sistem-absen
# 📸 SIABSEN — Sistem Informasi Absensi Siswa Berbasis Kamera & AI Face Recognition

> **Repositori Proyek Akhir Mandiri**
>
> **Mata Kuliah:** Rekayasa Perangkat Lunak — Semester 3
>
> **Program Studi:** S1 Teknik Informatika — STMIK IKMI Cirebon
>
> **Format Repositori:** `username/proyek-rpl-siabsen`

## 👨‍🎓 Identitas Proyek & Kelompok

* **Nama Aplikasi:** Sistem Absensi SIABSEN

* **Tema Topik Kelompok:** *E-Learning & Smart Education AI* (Sistem Informasi Absensi Siswa Berbasis Kamera dengan Manajemen Guru dan Mata Pelajaran)

* **Kelas:** TI-1D REGULER

* **Dosen Pengampu:** Yudhistira Arie Wijaya, M.Kom., CDS.

* **Sifat Pengerjaan:** Mandiri / *Full-Stack End-to-End Build*

### Daftar Anggota Kelompok (Tema Topik Sama)

* **Pemilik Repositori Individu:** `Fajar Febryano` (`41257190`)

| No | Nama Lengkap Anggota Kelompok | NIM | Peran Proyek | 
| ----- | ----- | ----- | ----- | 
| 1 | **Ahmad Firosy Fijri** | 41257176 | *Full-Stack Software Engineer (Individual Build)* | 
| 2 | **Arya Kusuma Firdaus** | 41257181 | *Full-Stack Software Engineer (Individual Build)* | 
| 3 | **Danish Akmal Marchielo** | 41257182 | *Full-Stack Software Engineer (Individual Build)* | 
| 4 | **Fajar Febryano** | 41257190 | *Full-Stack Software Engineer (Individual Build)* | 
| 5 | **Galang Marcellino** | 41257194 | *Full-Stack Software Engineer (Individual Build)* | 
| 6 | **Tredi** | 41257229 | *Full-Stack Software Engineer (Individual Build)* | 

## 📑 Daftar Isi

1. [Tautan Video Presentasi & Live Demo](#-tautan-video-presentasi--live-demo)

2. [Deskripsi Aplikasi & Spesifikasi Fitur AI](#-deskripsi-aplikasi--spesifikasi-fitur-ai)

3. [Fitur Utama Sistem (Role-Based)](#-fitur-utama-sistem-role-based)

4. [Arsitektur & Enam Komponen Perancangan Sistem](#-arsitektur--enam-komponen-perancangan-sistem)

   * [1. Use Case Diagram](#1-use-case-diagram)

   * [2. Activity Diagram (Alur Bisnis & Integrasi AI)](#2-activity-diagram-alur-bisnis--integrasi-ai)

   * [3. Class Diagram](#3-class-diagram)

   * [4. Sequence Diagram](#4-sequence-diagram)

   * [5. ERD (Entity Relationship Diagram) Basis Data](#5-erd-entity-relationship-diagram-basis-data)

   * [6. Prototipe Interaktif UI/UX Figma](#6-prototipe-interaktif-uiux-figma)

5. [Petunjuk Instalasi Aplikasi (Setup Instruction)](#-petunjuk-instalasi-aplikasi-setup-instruction)

6. [Pengujian Otomatis (Unit Testing) & CI/CD Pipeline](#-pengujian-otomatis-unit-testing--cicd-pipeline)

## 🎥 Tautan Video Presentasi & Live Demo

Seluruh tahapan presentasi (Progres 1, Progres 2, hingga *Live Demo Final* aplikasi web dan pengujian fitur AI secara *real-time*) telah didokumentasikan dan dapat diakses melalui tautan berikut:

| Tahapan Video | Materi Pembahasan Utama | Durasi Target | Tautan Video (YouTube) | 
| ----- | ----- | ----- | ----- | 
| **Video Progres 1** | Identifikasi Masalah, PRD/SRS, Kebutuhan Fungsional & Non-Fungsional, serta Peran Fitur AI | 3–5 Menit | [▶️ Tonton di YouTube](https://youtu.be/EFMjP4cdZJg) | 
| **Video Progres 2** | Bedah Logika 4 Diagram UML (Use Case, Activity, Class, Sequence), ERD, & Prototipe UI/UX Figma | 5–7 Menit | [▶️ Tonton di YouTube](https://youtu.be/EFMjP4cdZJg) | 
| **Video Final & Live Demo** | *Elevator Pitch*, Arsitektur Sistem, *Real-Time Live Demo* Aplikasi & AI Face Recognition, Unit Test, & CI/CD | 8–12 Menit | [▶️ Tonton di YouTube](https://youtu.be/EFMjP4cdZJg) | 

🔗 **Link Langsung Video Terintegrasi:** <https://youtu.be/EFMjP4cdZJg>

## 🤖 Deskripsi Aplikasi & Spesifikasi Fitur AI

### Deskripsi Aplikasi SIABSEN

**SIABSEN** adalah sistem informasi presensi siswa berbasis web yang mengintegrasikan tangkapan kamera perangkat secara langsung (*real-time camera capture*) dengan manajemen akademik sekolah yang mencakup pengaturan kelas, mata pelajaran, jadwal pelajaran, serta penugasan guru pengampu. Aplikasi ini dirancang untuk mencegah kecurangan titip absen, mempercepat rekapitulasi kehadiran oleh guru, dan menyajikan laporan kehadiran yang akurat.

### Spesifikasi Fitur AI Utama: *AI Face Recognition* (Computer Vision)

Sebagai implementasi kecerdasan artifisial (*Artificial Intelligence*) pada sistem informasi pendidikan, **SIABSEN** menanamkan fitur **AI Face Recognition / Face Verification** secara *real-time*:

* **Deteksi & Ekstraksi Wajah Otomatis:** Saat siswa mengaktifkan kamera pada menu absensi, modul AI mendeteksi keberadaan wajah pada *frame* kamera sebelum tombol kirim diaktifkan.

* **Pencocokan Biometrik (*Face Matching*):** Citra wajah yang diambil oleh siswa dikirim ke layanan pemrosesan AI untuk dibandingkan tingkat kemiripannya (*similarity score*) dengan foto referensi profil siswa di basis data.

* **Validasi Kehadiran Cerdas:** Sistem secara otomatis menyetujui atau menolak pencatatan absensi berdasarkan ambang batas (*threshold*) kecocokan wajah, sekaligus menyimpan bukti foto berstempel waktu (*timestamp*) untuk diaudit oleh guru.

## ✨ Fitur Utama Sistem (Role-Based)

Fitur di dalam aplikasi **SIABSEN** dibagi berdasarkan hak akses (*Role-Based Access Control*) untuk tiga aktor pengguna:

### 1. 👨‍🎓 Aktor Siswa

* **Autentikasi Akun:** Login aman ke portal siswa.

* **Absensi Kamera Berbasis AI:** Mengambil swafoto kehadiran melalui *browser* dengan verifikasi *AI Face Recognition*.

* **Status Absensi Harian:** Melihat status keberhasilan dan skor verifikasi absensi pada hari berjalan.

* **Riwayat Absensi:** Memantau daftar riwayat kehadiran pribadi berdasarkan tanggal dan mata pelajaran.

### 2. 👩‍🏫 Aktor Guru

* **Dashboard & Jadwal Mengajar:** Melihat daftar mata pelajaran yang diampu beserta kelas yang diajar.

* **Monitoring Rekap Absensi:** Memeriksa daftar kehadiran siswa berdasarkan filter kelas, mata pelajaran, dan tanggal.

* **Verifikasi Bukti Foto:** Melihat detail foto bukti absensi yang diunggah siswa beserta status verifikasi AI.

* **Ekspor Laporan:** Mengunduh rekapitulasi laporan kehadiran siswa.

### 3. 🛠️ Aktor Admin

* **Manajemen Data Master (CRUD):** Mengelola data induk Siswa, Guru, Kelas, dan Mata Pelajaran.

* **Manajemen Penugasan & Jadwal:** Mengatur guru pengampu (*Teacher Assignment*) dan menyusun jadwal pelajaran sekolah.

* **Audit Absensi Menyeluruh:** Memantau seluruh transaksi data absensi dari semua kelas.

## 🏗️ Arsitektur & Enam Komponen Perancangan Sistem

Perancangan sistem mengacu pada standar *Software Design Document* (SDD) dengan menjaga konsistensi penamaan entitas, aktor, dan alur pesan di seluruh diagram.

### 1. Use Case Diagram

Menggambarkan interaksi antara tiga aktor utama (**Siswa**, **Guru**, dan **Admin**) terhadap seluruh fungsionalitas sistem serta membatasi hak akses masing-masing pengguna sesuai perannya.

### 2. Activity Diagram (Alur Bisnis & Integrasi AI)

Menggambarkan urutan aktivitas sistem dari awal hingga akhir:

* **Alur Absensi Siswa & AI:** Siswa membuka web $\rightarrow$ Login & validasi akun $\rightarrow$ Buka menu absensi $\rightarrow$ Sistem memeriksa status absen hari ini $\rightarrow$ Kamera diaktifkan & siswa mengambil foto $\rightarrow$ Sistem mengirim foto ke modul **AI Face Recognition** $\rightarrow$ AI mencocokkan wajah dengan data referensi $\rightarrow$ Sistem menyimpan data absensi & menampilkan status verifikasi kehadiran.

* **Alur Guru:** Login & validasi hak akses $\rightarrow$ Buka dashboard $\rightarrow$ Pilih mata pelajaran, kelas, dan tanggal $\rightarrow$ Sistem menampilkan rekap absensi, detail foto bukti, & opsi unduh laporan.

* **Alur Admin:** Login $\rightarrow$ Buka dashboard $\rightarrow$ Kelola data master (siswa, guru, kelas, mapel) $\rightarrow$ Atur guru pengampu & jadwal pelajaran $\rightarrow$ Sistem menyimpan konfigurasi ke *database*.

### 3. Class Diagram

Memodelkan struktur program berorientasi objek dengan menerapkan prinsip modularitas:

| Nama Class | Tanggung Jawab / Fungsi Utama | 
| ----- | ----- | 
| `User` | Mengelola kredensial akun login dan *role* pengguna | 
| `Student` | Menyimpan atribut profil siswa dan data referensi wajah | 
| `Teacher` | Menyimpan atribut profil dan identitas guru | 
| `SchoolClass` | Menyimpan entitas data kelas / rombongan belajar | 
| `Subject` | Menyimpan entitas data mata pelajaran | 
| `TeacherAssignment` | Menghubungkan relasi antara guru, kelas, dan mata pelajaran | 
| `Schedule` | Menyimpan jadwal jam pelajaran berdasarkan penugasan guru | 
| `Attendance` | Mengelola transaksi absensi, foto bukti, dan status verifikasi AI | 

**Spesifikasi Detail `Class Attendance`:**

* **Atribut:** `attendance_id`, `student_id`, `tanggal`, `waktu_absensi`, `foto`, `status`

* **Method:** `createAttendance()`, `checkAttendance()`, `getAttendanceHistory()`

### 4. Sequence Diagram

Menunjukkan urutan pertukaran pesan (*message passing*) antar-komponen berdasarkan waktu untuk skenario **Absensi Kamera Siswa**:

1. **Siswa** meminta halaman login dan melakukan autentikasi ke **Database**.

2. **Siswa** membuka menu absensi; sistem memeriksa catatan absensi hari ini.

3. **Browser (Frontend)** meminta izin akses kamera dan menangkap citra foto wajah siswa.

4. **Browser** mengirimkan payload foto ke **Controller (Backend)**.

5. **Controller** meneruskan citra wajah ke **AI Face Recognition Service** untuk memvalidasi kecocokan wajah.

6. Setelah terverifikasi, **Model** menyimpan file foto dan mencatat transaksi ke **Database**.

7. **Sistem** mengembalikan respons notifikasi absensi berhasil ke layar **Siswa**.

### 5. ERD (Entity Relationship Diagram) Basis Data

Skema basis data relasional dirancang untuk menghindari redundansi data:

| Nama Tabel | Primary Key | Relasi & Keterangan | 
| ----- | ----- | ----- | 
| `users` | `id` | Menyimpan akun autentikasi seluruh pengguna | 
| `students` | `id` | Berelasi ke `users` dan `classes` | 
| `teachers` | `id` | Berelasi ke `users` | 
| `classes` | `id` | Memiliki relasi $1:N$ terhadap tabel `students` | 
| `subjects` | `id` | Memiliki relasi $1:N$ terhadap tabel `teacher_assignments` | 
| `teacher_assignments` | `id` | Tabel penghubung antara `teachers`, `subjects`, dan `classes` | 
| `schedules` | `id` | Memiliki relasi $N:1$ terhadap `teacher_assignments` | 
| `attendance` | `id` | Memiliki relasi $N:1$ terhadap `students` (riwayat absensi) | 

### 6. Prototipe Interaktif UI/UX Figma

Rancangan antarmuka aplikasi mencakup **11 halaman utama** yang saling terhubung secara interaktif:

* **Umum:** Halaman Login & Dashboard dinamis sesuai *role*.

* **Siswa:** Halaman Absensi Kamera (dengan *viewfinder* & *preview* foto) serta Halaman Riwayat Absensi.

* **Guru:** Halaman Rekap Absensi, Detail Bukti Foto Absensi, dan Unduh Laporan.

* **Admin:** Halaman Manajemen Data Siswa, Data Guru, Data Kelas, Mata Pelajaran, dan Jadwal Pelajaran.

## ⚙️ Petunjuk Instalasi Aplikasi (Setup Instruction)

Ikuti langkah-langkah berikut untuk menjalankan aplikasi **SIABSEN** di komputer lokal (*Local Development Environment*):

### 1. Prasyarat Sistem (*Prerequisites*)

Pastikan perangkat Anda telah terinstal:

* **Git**

* **Node.js** (v18+) & **NPM** *(jika menggunakan stack JavaScript/Node.js)* atau **XAMPP / Laragon (PHP 8.x & MySQL)** *(jika menggunakan stack PHP)*

* **Web Browser Modern** (Google Chrome / Microsoft Edge) dengan izin akses *Webcam* aktif.

### 2. Clone Repositori

Buka terminal dan jalankan perintah berikut:

```
git clone https://github.com/username/proyek-rpl-siabsen.git
cd proyek-rpl-siabsen

```

### 3. Konfigurasi & Menjalankan Aplikasi

#### Opsi A — Jika Proyek Berbasis Node.js / Vite / Next.js (Terdapat file `package.json`)

1. Instal seluruh dependensi paket:

   ```
   npm install
   
   ```

2. Salin konfigurasi *environment* (jika ada file `.env.example`):

   ```
   cp .env.example .env
   
   ```

3. Jalankan server pengembangan lokal:

   ```
   npm run dev
   
   ```

4. Buka browser dan akses alamat yang muncul di terminal (umumnya `http://localhost:3000` atau `http://localhost:5173`).

#### Opsi B — Jika Proyek Berbasis PHP & MySQL / HTML Statis

1. Pindahkan folder proyek ke dalam direktori `htdocs` (XAMPP) atau `www` (Laragon).

2. Buka **phpMyAdmin** (`http://localhost/phpmyadmin`), buat *database* baru bernama `db_siabsen`, lalu impor berkas `.sql` yang tersedia di dalam folder database proyek.

3. Sesuaikan konfigurasi koneksi *database* pada file konfigurasi aplikasi.

4. Buka browser dan akses `http://localhost/proyek-rpl-siabsen`.

## 🧪 Pengujian Otomatis (Unit Testing) & CI/CD Pipeline

Proyek ini dilengkapi dengan pengujian fungsionalitas otomatis serta integrasi *Continuous Integration / Continuous Deployment* (CI/CD) menggunakan **GitHub Actions**:

* **Menjalankan Unit Test secara Lokal:**

  ```
  npm test
  
  ```

* **Konfigurasi CI/CD Pipeline:**

  Tersedia pada direktori `.github/workflows/ci.yml` yang secara otomatis menjalankan pemeriksaan kode dan skrip pengujian setiap kali terdapat `git push` atau `pull request` ke cabang utama (`main`).
