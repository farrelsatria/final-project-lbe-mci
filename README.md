# Student Academic Performance Segmentation: Habit-Driven Clustering Analysis

**Kelompok 3**
| Nama Lengkap | NRP |
| :--- | :--- |
| Farrel Satria Mukti | 5025251138 |
| Made Joshua Ama Ede | 5025251150 |
| Dewa Ngakan Putu Sunyananda T. | 5025251152 |
| Wanhardo Jawak | 5025251155 |
| Fawwas Razzan Sulfi Andreyawan | 5025251202 |

## Latar Belakang Proyek
Repositori ini berisi kode dan dokumentasi untuk **Final Project** dari program **Lab Based Education (LBE)**. Program LBE ini diselenggarakan oleh **Laboratorium Manajemen Cerdas Informasi (MCI)** di Departemen **Teknik Informatika, Institut Teknologi Sepuluh Nopember (ITS)**. 

## Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis dan mengelompokkan (segmentasi) siswa berdasarkan pola kebiasaan, kondisi psikososial, dan performa akademik. Pertanyaan utama yang dijawab melalui analisis ini adalah bagaimana institusi dapat merumuskan intervensi akademik terpersonalisasi untuk setiap segmen siswa guna meminimalisir stres dan memaksimalkan capaian akademik.

## Rincian Dataset
Analisis dilakukan menggunakan dataset `dustinia_bersekolah.csv` yang memiliki rincian sebagai berikut:
* **Total Data**: 10.000 baris data.
* **Jumlah Variabel**: 28 variabel.
* **Kategori Data**: Terbagi menjadi 3 kategori utama:
  * **Demografi**: Pendapatan keluarga, tingkat pendidikan orang tua, tipe sekolah.
  * **Kondisi**: Jam belajar & tidur, tingkat kehadiran, motivasi, tingkat stres, tutoring.
  * **Akademik**: GPA, Reading, Writing, Math, Science.

## Fitur Terpilih (Feature Selection)
Untuk membangun model segmentasi, kami memilih empat fitur utama yang mewakili kombinasi utuh antara pola belajar, kedisiplinan, dan performa akademik siswa:
1. **Sleep Hours**
2. **Study Hours**
3. **Stress Level**
4. **GPA**

Pemilihan fitur ini ditujukan untuk memetakan secara bersamaan proses dari sisi usaha (effort) dan kesejahteraan (wellbeing) siswa, sekaligus hasil akhir berupa capaian akademik.

## Struktur Repositori
```text
.
├── dustinia_bersekolah.csv                     # Dataset utama
├── Kelompok 3_Notebook_FP LBE MCI 2026.ipynb   # Source code analisis dan clustering
├── Kelompok 3_Deck_FP LBE MCI 2026.pdf         # Slide presentasi final project
├── requirements.txt                            # Daftar dependensi Python
└── README.md                                   # Dokumentasi repositori
```

## Cara Menjalankan Proyek Secara Lokal

Berikut adalah tahapan untuk menjalankan proyek ini di komputer Anda, untuk pengguna **macOS**, **Windows**, dan **Linux**.

### 1. Clone Repositori

Unduh repositori ini ke komputer lokal Anda dengan menjalankan perintah berikut di Terminal (macOS/Linux) atau Command Prompt/PowerShell (Windows):

```bash
git clone https://github.com/farrelsatria/final-project-lbe-mci.git
cd final-project-lbe-mci
```

### 2. Persiapkan Lingkungan Virtual (Direkomendasikan)

Untuk menghindari konflik antar package sistem, buat dan aktifkan virtual environment sesuai sistem operasi Anda.

**macOS / Linux**

```bash
# Membuat virtual environment bernama .venv
python3 -m venv .venv

# Mengaktifkan virtual environment
source .venv/bin/activate
```

**Windows (Command Prompt)**

```bash
# Membuat virtual environment bernama .venv
python -m venv .venv

# Mengaktifkan virtual environment
.venv\Scripts\activate.bat
```

**Windows (PowerShell)**

```bash
# Membuat virtual environment bernama .venv
python -m venv .venv

# Mengaktifkan virtual environment
.venv\Scripts\Activate.ps1
```

> **Catatan untuk PowerShell:** jika muncul error terkait *execution policy*, jalankan perintah berikut sekali saja sebelum mengaktifkan environment:
> ```bash
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

Setelah aktif, biasanya akan muncul tanda `(.venv)` di awal baris terminal Anda.

### 3. Instalasi Dependensi

Instal seluruh library yang dibutuhkan menggunakan file `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 4. Jalankan Jupyter Notebook

Buka dan jalankan file notebook menggunakan Jupyter, atau langsung melalui Visual Studio Code.

**Melalui Jupyter Notebook**

```bash
jupyter notebook "Kelompok 3_Notebook_FP LBE MCI 2026.ipynb"
```

**Melalui Visual Studio Code**

1. Buka folder proyek di VS Code (`File → Open Folder...`).
2. Buka file `Kelompok 3_Notebook_FP LBE MCI 2026.ipynb`.
3. Pastikan kernel Python yang dipilih (pojok kanan atas) adalah kernel dari `.venv` yang sudah dibuat sebelumnya.
4. Jalankan tiap cell secara berurutan.

### 5. Menonaktifkan Virtual Environment (Opsional)

Setelah selesai bekerja, environment dapat dinonaktifkan dengan perintah berikut (berlaku untuk semua OS):

```bash
deactivate
```