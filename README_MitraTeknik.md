# 🔧 Analisis Bisnis MitraTeknik Otomotif
### *Business Analytics Portfolio Project — Junior Data & Business Analyst*

---

> **Tentang Proyek Ini**
> Proyek ini merupakan studi kasus analisis bisnis komprehensif untuk **MitraTeknik Otomotif**, perusahaan jasa servis kendaraan yang berspesialisasi pada layanan sistem AC dan Non-AC dengan jaringan 200+ dealer mitra di seluruh Indonesia.
>
> Analisis mencakup data operasional periode **Januari 2024 – Mei 2025**, menghasilkan laporan strategis berbasis data yang mendukung pengambilan keputusan manajemen. Seluruh data dalam proyek ini adalah **data dummy** yang dibuat untuk keperluan portofolio, dengan pola dan struktur yang mencerminkan kondisi riil industri otomotif.

---

## 📊 Ringkasan Eksekutif

| Metrik | Nilai |
|--------|-------|
| 🔢 Total Transaksi | **100** (Jan 2024 – Mei 2025) |
| 💰 Total Pendapatan | **Rp 158,8 Juta** |
| ⭐ Rata-rata Rating | **4,34** (target 4,20 ✓) |
| ✅ Completion Rate | **90,0%** (AC: 94,3% \| Non-AC: 85,1%) |
| 🏢 Dealer Aktif | **15 dealer** di **12 provinsi** |
| 👨‍🔧 Teknisi Aktif | **10 teknisi** bersertifikasi ATC L1–L3 |
| 📈 Pencapaian KPI 2024 | **10/10 KPI tercapai** (rata-rata 108,6%) |

---

## 🎯 Tujuan Analisis

Laporan ini disusun untuk menjawab empat pertanyaan bisnis utama:

**A. Volume & Distribusi** — Layanan apa yang paling diminati? Dealer dan wilayah mana yang berkinerja terbaik?

**B. Keuangan** — Bagaimana struktur pendapatan? Apa revenue driver utama? Seperti apa pola seasonality-nya?

**C. Kualitas Layanan** — Faktor apa yang mempengaruhi kepuasan pelanggan? Di mana gap completion rate terjadi?

**D. Monitoring Business Plan** — Seberapa jauh pencapaian KPI 2024? KPI mana yang at-risk di 2025?

---

## 🗂️ Struktur File Proyek

```
📦 mitrateknik-otomotif-analysis/
 ├── 📑 2025_Strategic_Growth_Navigation.pdf         # Presentasi strategis 15 slide
 ├── 📄 Laporan_Analisis_Bisnis_MitraTeknik.pdf      # Laporan lengkap 21 halaman
 ├── 📊 MitraTeknik_Otomotif_Data_Portofolio.xlsx   # Dataset sumber (4 sheet)
 └── 📄 README.md
```

---

## 📁 Dokumentasi File

### 1. `MitraTeknik_Otomotif_Data_Portofolio.xlsx` — Dataset Utama

File Excel berisi **4 sheet** yang menjadi sumber data seluruh analisis:

| Sheet | Konten | Baris | Kolom | Digunakan untuk |
|-------|--------|-------|-------|-----------------|
| **Data Transaksi Servis** | Rekaman transaksi individual | 100 | 20 | Analisis A, B, C |
| **Ringkasan KPI** | Dashboard KPI agregat | 23 | 6 | Validasi kalkulasi |
| **Analisis Regional** | Kinerja per provinsi | 12 | 5 | Analisis geografis |
| **Monitoring Business Plan** | Target vs realisasi KPI | 10 | 7 | Analisis D |

**Kolom Kunci — Sheet Data Transaksi:**

| Kolom | Tipe | Deskripsi |
|-------|------|-----------|
| `ID_Transaksi` | STRING | ID unik per transaksi |
| `Tanggal` | DATE | Tanggal servis dilakukan |
| `Nama_Dealer` | STRING | Dealer tempat servis |
| `Provinsi` | STRING | Lokasi dealer |
| `Nama_Teknisi` | STRING | Teknisi yang menangani |
| `Sertifikasi` | STRING | Level ATC teknisi (L1/L2/L3) |
| `Jenis_Layanan` | STRING | Kategori servis (AC/Non-AC) |
| `Nama_Layanan` | STRING | Detail jenis servis spesifik |
| `Pendapatan` | INT | Nilai transaksi (Rp) |
| `Biaya_Jasa` | INT | Komponen biaya jasa |
| `Biaya_Suku_Cadang` | INT | Komponen biaya suku cadang |
| `Durasi_Servis` | FLOAT | Lama pengerjaan (jam) |
| `Status` | STRING | Selesai / Tidak Selesai |
| `Rating_Pelanggan` | FLOAT | Kepuasan pelanggan (1–5) |
| `Komplain` | STRING | Ada / Tidak ada komplain |

**Sample Data:**
```
ID_Transaksi | Tanggal    | Dealer              | Provinsi   | Teknisi       | Layanan              | Pendapatan  | Status  | Rating
TRX-001      | 2024-01-05 | Auto2000 Jaksel     | DKI Jakarta| Dwi Rahmadi   | Servis AC Mobil      | Rp 1.450.000| Selesai | 4.5
TRX-013      | 2024-02-12 | Mitsubishi Bogor    | Jawa Barat | Joko Susilo   | Non-AC Tune Up       | Rp 2.100.000| Selesai | 4.2
TRX-047      | 2024-08-20 | Nissan Makassar     | Sulsel     | Hendra Wijaya | Pembersihan Evap.    | Rp 1.200.000| Selesai | 5.0
TRX-089      | 2025-03-15 | Honda Bekasi Galaxy | Jawa Barat | Fajar Nugroho | Servis Rem           | Rp 1.800.000| Tdk Sls | 3.5
```

**KPI Monitoring (sample):**
```
Indikator KPI         | Target 2024 | Realisasi 2024 | Capaian | Status 2024 | Target 2025 | YTD 2025 | Status 2025
Total Transaksi       | 5.000       | 5.340          | 106,8%  | ✓ Tercapai  | 6.500       | 2.890    | At-risk
Pendapatan (Rp Jt)    | 12.500      | 13.200         | 105,6%  | ✓ Tercapai  | 16.000      | 7.450    | At-risk
Rata-rata Rating      | 4,20        | 4,40           | 104,8%  | ✓ Tercapai  | 4,50        | 4,50     | On-track
Pelatihan Teknis (sesi)| 24         | 26             | 108,3%  | ✓ Tercapai  | 30          | 14       | ⚠ Underperforming
```

---

### 2. `Laporan_Analisis_Bisnis_MitraTeknik.pdf` — Laporan Komprehensif

Laporan tertulis **21 halaman** yang disusun sebagai **portofolio Junior Business Analyst**. Terdiri dari 8 bagian utama:

| Bab | Judul | Konten |
|-----|-------|--------|
| 01 | **Executive Summary** | Ikhtisar KPI, temuan kritis, dan top-3 rekomendasi dalam 1 halaman |
| 02 | **Latar Belakang & Tujuan** | Profil perusahaan, scope analisis, batasan data |
| 03 | **Metodologi** | Framework (5W+1H, SWOT, KPI Scorecard, Risk Matrix), tools, sumber data |
| 04 | **Temuan Utama** | Analisis A-D: volume, keuangan, kualitas, monitoring business plan |
| 05 | **Tren & Pola** | Seasonality, anomali, distribusi geografis, tren pertumbuhan kuartalan |
| 06 | **Risiko & Peluang** | Analisis SWOT berbasis data + risk matrix probabilitas vs dampak |
| 07 | **Rekomendasi Strategis** | 6 rekomendasi dengan target, PIC, estimasi biaya, dan timeline |
| 08 | **Lampiran** | Data lengkap per dealer, performa teknisi, glosarium istilah |

**Temuan Kritis:**

- **Jabar Paradox**: Jawa Barat memiliki volume tertinggi (28 trx, 28%) namun rating terendah nasional (4,18) — indikasi krisis *over-capacity* teknisi
- **Servis Rem Bottleneck**: Completion rate Servis Rem hanya 69,2% vs rata-rata Non-AC 85,1% — mengindikasikan isu struktural rantai pasok komponen
- **SDM At-risk**: Pelatihan teknisi YTD 2025 baru 46,7% (14/30 sesi) — satu-satunya KPI berstatus *Underperforming*
- **Volume 2025 At-risk**: YTD hanya 44,5% dari target 6.500 transaksi — membutuhkan akselerasi signifikan di H2 2025

**Distribusi 15 Dealer Aktif:**

| Provinsi | Dealer Utama | Transaksi | Rating |
|----------|-------------|-----------|--------|
| DKI Jakarta | Auto2000 Jakarta Selatan | 16 | 4,28 |
| Jawa Barat | Astra Daihatsu Bandung, Honda Bekasi, Toyota Depok, Mitsubishi Bogor | 28 | 4,18 |
| Banten | Auto2000 Tangerang Selatan | 8 | 4,50 |
| Sulawesi Selatan | Nissan Makassar | 9 | 4,33 |
| Kalimantan Timur | Daihatsu Balikpapan | 7 | 4,47 |
| Sumatera Selatan | Suzuki Palembang | 5 | 4,54 ⭐ |
| Bali | Wuling Denpasar | 3 | 4,43 |
| ... | ... | ... | ... |

**Performa 10 Teknisi:**

| Ranking | Teknisi | Sertifikasi | Transaksi | Rating | Status |
|---------|---------|-------------|-----------|--------|--------|
| 1 | Hendra Wijaya | ATC Level 1 | 8 | 4,44 | Ahli |
| 2 | Dwi Rahmadi | ATC Level 2 | 16 | 4,39 | Bintang |
| 3 | Joko Susilo | ATC Level 1 | 13 | 4,42 | Bintang |
| ... | ... | ... | ... | ... | ... |
| 10 | **Fajar Nugroho** | ATC Level 2 | 9 | **4,02** | ⚠ Perlu Coaching |

---

### 3. `2025_Strategic_Growth_Navigation.pdf` — Presentasi Strategis

Presentasi eksekutif **15 slide** bertema *"Navigasi Pertumbuhan 2025"* yang dibuat menggunakan **NotebookLM**. Dirancang untuk penyampaian kepada level manajemen senior.

**Alur Narasi Presentasi:**

| Slide | Judul | Pesan Utama |
|-------|-------|-------------|
| 1 | Cover | Navigasi Pertumbuhan 2025: Membedah 2024, Mendiagnosis 2025, Peta Jalan Eksekutif |
| 2 | Rekam Jejak Operasional | 100 trx · Rp 158,8 Jt · Rating 4,34 (Jan 2024–Mei 2025) |
| 3 | Kinerja 2024 ✅ | 10/10 KPI tercapai · 108,6% rata-rata · Komplain turun ke 3,8% |
| 4 | Peringatan Dini 2025 ⚠️ | Volume 44,5% target · Pendapatan Rp 7,45 M (at-risk Rp 16 M) |
| 5 | Kesenjangan Sistemik | Servis Rem CR 69,2% vs AC 100% — gap 30 poin |
| 6 | Paradoks Geografis | Jabar 28 trx rating 4,18 vs Sumsel 5 trx rating 4,54 |
| 7 | Pemetaan Kapasitas Teknisi | Scatter plot: Fajar Nugroho titik merah kritis |
| 8 | Irama Pendapatan | Seasonality: peak Q4, trough Feb & Apr |
| 9 | Tesis Utama 2025 | Masalah = Kebocoran Kapasitas + Ketidakstabilan SOP Non-AC |
| 10 | Risk Matrix | Matriks Probabilitas vs Dampak (5 isu dipetakan) |
| 11 | Resolusi Jangka Pendek (0–3 bln) | Coaching Fajar · Pelatihan Hybrid · Kampanye Feb/Apr |
| 12 | Resolusi Jangka Menengah (3–6 bln) | Ekspansi Luar Jawa · Redistribusi Teknisi Jabar |
| 13 | Resolusi Jangka Panjang (6–12 bln) | Audit Rantai Pasok Rem · SOP Baru · Dashboard Real-time |
| 14 | Roadmap 12 Bulan | Gantt chart 4 fase: Reaksi Cepat → Stabilisasi → Ekspansi → Pematangan |
| 15 | Visi Eksekusi | 3 roda gigi: Kapasitas · Keunggulan Operasional · Kualitas Tim |

---

## 🔍 Key Findings

### ✅ Pencapaian 2024
- **10/10 KPI Business Plan 2024** terlampaui dengan rata-rata pencapaian **108,6%**
- Rating kepuasan **4,34** — melampaui target 4,20 secara konsisten
- Tingkat komplain turun ke **3,8%** (jauh di bawah batas toleransi 5,0%)
- Completion Rate AC **94,3%** — hampir sempurna

### ⚠️ Sinyal Peringatan 2025
- Volume transaksi YTD hanya **2.890** dari target **6.500** (44,5%) — status At-risk
- Pendapatan YTD **Rp 7,45 M** dari target **Rp 16 M** (46,6%) — status At-risk
- Pelatihan teknisi baru **14/30 sesi** (46,7%) — satu-satunya KPI *Underperforming*

### 🔴 Anomali Kritis
| Anomali | Temuan | Hipotesis |
|---------|--------|-----------|
| **Jabar Paradox** | Volume tertinggi (28 trx) tapi rating terendah (4,18) | Teknisi over-capacity menurunkan standar kualitas |
| **Servis Rem CR** | Completion rate hanya 69,2% vs rata-rata 90% | Isu struktural rantai pasok atau SOP |
| **ATC L1 Unggul** | Level 1 (4,40) lebih tinggi dari Level 2 (4,30) dan Level 3 (4,32) | Servis dasar = ekspektasi pelanggan lebih terkelola |

### 💡 Seasonality
- **Peak**: Q4 (Okt–Jan) — musim hujan mendorong permintaan servis AC. Q4 2024 = Rp 45,1 Jt (28% pendapatan tahunan)
- **Trough**: Februari & April — konsisten hanya 3 transaksi/bulan (73% di bawah rata-rata)

---

## 🎯 Rekomendasi Strategis (6 Prioritas)

| # | Prioritas | Horizon | Tindakan | Target |
|---|-----------|---------|----------|--------|
| 1 | **Coaching Fajar Nugroho** | 0–30 hari | Mentoring 1-on-1 dengan Hendra Wijaya selama 30 hari | Rating ≥ 4,20 dalam 60 hari |
| 2 | **Akselerasi Pelatihan** | 1–2 bulan | Jadwalkan 16 sesi tersisa dengan format hybrid | 30 sesi tuntas per Feb 2026 |
| 3 | **Kampanye Feb & Apr** | 1–3 bulan | Paket bundling AC+Oli diskon 15% di bulan sepi | +100% volume → 6 trx/bulan |
| 4 | **Ekspansi Luar Jawa** | 3–6 bulan | Tambah dealer di Bali, Sumut, Jatim (rating 4,42–4,54) | +Rp 25–35 Jt/kuartal |
| 5 | **Redistribusi Teknisi Jabar** | 3–6 bulan | Rekrut 2–3 teknisi ATC L2 + sistem antrian digital | Rating Jabar ≥ 4,30 dalam 90 hari |
| 6 | **Transformasi Non-AC** | 6–12 bulan | Audit rantai pasok rem + SOP 12 poin + dashboard real-time | Servis Rem CR ≥ 85% · Non-AC CR ≥ 90% |

---

## 🛠️ Tools & Metodologi

| Kategori | Tools / Framework |
|----------|------------------|
| **Data Processing** | Microsoft Excel (Pivot Table, VLOOKUP, Chart) |
| **Statistical Analysis** | Python (Pandas) |
| **Data Visualization** | Chart.js, Excel Charts |
| **Presentation** | NotebookLM (AI-assisted slide generation) |
| **Analytical Framework** | 5W+1H, SWOT, KPI Scorecard, Risk Matrix, Trend Analysis |
| **Report Format** | HTML → PDF (laporan terstruktur) |
| **Version Control** | Git & GitHub |

---

## 📐 Struktur Analisis

```
INPUT DATA
    │
    ├── Data Transaksi (100 rows × 20 col)
    ├── Ringkasan KPI (23 rows × 6 col)
    ├── Analisis Regional (12 rows × 5 col)
    └── Monitoring Business Plan (10 rows × 7 col)
    │
    ▼
PROSES ANALISIS
    │
    ├── A. Analisis Deskriptif ──── distribusi, frekuensi, proporsi
    ├── B. Analisis Diagnostik ──── pola, korelasi, anomali
    └── C. Analisis Preskriptif ─── rekomendasi + estimasi dampak
    │
    ▼
OUTPUT
    │
    ├── 📊 Excel Dashboard (MitraTeknik_Otomotif_Data_Portofolio.xlsx)
    ├── 📄 Laporan Analisis 21 hal. (Laporan_Analisis_Bisnis.pdf)
    └── 📑 Presentasi Eksekutif 15 slide (2025_Strategic_Growth_Navigation.pdf)
```

---

## 🚀 Cara Menggunakan

### Clone Repository
```bash
git clone https://github.com/username/mitrateknik-business-analysis.git
cd mitrateknik-business-analysis
```

### Eksplorasi Data dengan Python
```python
import pandas as pd

# Load dataset
df = pd.read_excel('MitraTeknik_Otomotif_Data_Portofolio.xlsx',
                   sheet_name='Data Transaksi Servis')

# Quick stats
print(df.describe())
print(f"Total pendapatan: Rp {df['Pendapatan'].sum():,.0f}")
print(f"Rata-rata rating: {df['Rating_Pelanggan'].mean():.2f}")

# Analisis per provinsi
df.groupby('Provinsi').agg(
    total_trx=('ID_Transaksi', 'count'),
    avg_rating=('Rating_Pelanggan', 'mean'),
    total_pendapatan=('Pendapatan', 'sum')
).sort_values('total_trx', ascending=False)

# Completion rate per layanan
df.groupby('Nama_Layanan').apply(
    lambda x: (x['Status'] == 'Selesai').mean() * 100
).round(1).sort_values()
```

---

## 👤 Tentang Proyek Ini

Proyek ini saya kerjakan sebagai **studi kasus mandiri** untuk membangun portofolio sebagai **Junior Business Analyst / Data Analyst**. Saya memilih industri otomotif karena familiar dengan dinamika bisnisnya — data berbasis layanan, jaringan dealer, dan manajemen SDM teknisi.

**Skill yang didemonstrasikan dalam proyek ini:**
- 📊 Analisis data multidimensi (volume, keuangan, kualitas, KPI)
- 📈 Identifikasi pola, anomali, dan seasonality dari data historis
- 🗺️ Analisis geospasial dan distribusi regional
- 🎯 Penyusunan rekomendasi strategis berbasis data (data-driven decision making)
- 📄 Komunikasi insight kepada berbagai level audiens (laporan teknis + presentasi eksekutif)
- 🛠️ Data storytelling — mengubah angka menjadi narasi bisnis yang actionable

**Connect with me:**
- 💼 [LinkedIn](https://linkedin.com/in/username)
- 🐙 [GitHub](https://github.com/username)
- 📧 email@example.com

---

## 📌 Disclaimer

> Seluruh data dalam proyek ini adalah **data dummy / sintetis** yang dibuat khusus untuk keperluan portofolio. Nama dealer, teknisi, dan angka finansial adalah fiktif. Perusahaan "MitraTeknik Otomotif" adalah entitas fiktif. Pola dan struktur data dirancang untuk mencerminkan kondisi nyata industri jasa otomotif Indonesia.

---

## 📜 Lisensi

Proyek ini bersifat open portfolio. Bebas digunakan sebagai referensi belajar. Mohon cantumkan credit jika digunakan ulang.

---

*⭐ Jika proyek ini menginspirasi, silakan beri bintang!*

*Last updated: Mei 2026 · Disusun oleh: Junior Business Analyst*
