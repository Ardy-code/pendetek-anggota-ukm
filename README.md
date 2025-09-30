# Prediksi Keaktifan Anggota UKM Kampus

## Elevator Pitch
Sebuah sistem analitik sederhana berbasis machine learning untuk memprediksi tingkat keaktifan anggota UKM di kampus. Sistem ini membantu pengurus UKM mengidentifikasi anggota yang aktif dan tidak aktif berdasarkan data seperti jumlah kegiatan, jabatan, kehadiran rapat, dan tugas. Dengan model ini, pengurus dapat membuat kebijakan yang lebih tepat sasaran untuk meningkatkan partisipasi mahasiswa.

## Problem Statement
Pengurus UKM sering kesulitan membedakan anggota yang aktif dan yang mulai tidak aktif. Hal ini berdampak pada pembagian tugas yang tidak merata dan menurunkan kinerja organisasi.  
**Nilai bagi pengguna:** memudahkan pengurus dalam melakukan monitoring anggota.  
**Nilai bagi organisasi:** mendukung strategi peningkatan keaktifan anggota dan pengelolaan SDM yang lebih efisien.

> **Catatan:** Data yang digunakan masih berupa **dummy dataset**, bukan data riil mahasiswa. Data dummy dibuat agar tidak melibatkan informasi pribadi dan hanya dipakai untuk eksplorasi awal.

## Scope

**In-Scope:**
- Prediksi keaktifan anggota UKM (aktif vs tidak aktif).
- Menggunakan dataset dummy (jumlah kegiatan, jabatan, kehadiran, tugas, fakultas).
- Implementasi Logistic Regression sebagai model baseline.

**Out-of-Scope:**
- Data riil mahasiswa (privasi).
- Prediksi keaktifan berbasis faktor psikologis atau motivasi personal.
- Integrasi ke sistem informasi kampus (masih tahap eksplorasi).

## Metrik
- **Baseline:** F1-Score = 0.50 (target awal minimal).  
- **Target:** Model mencapai F1-Score ≥ 0.70.  
- **Evaluasi:** Menggunakan F1-Score karena dataset bisa tidak seimbang (jumlah anggota aktif vs tidak aktif berbeda).

## Data
- Dataset dummy berisi 300 mahasiswa anggota UKM.  
- Fitur yang digunakan:  
  - Jumlah kegiatan diikuti  
  - Jabatan (Anggota / Pengurus)  
  - Kehadiran rapat  
  - Tugas terlambat  
  - Fakultas  
- Label: `Aktif` (1 = aktif, 0 = tidak aktif)  
- Data ini **sepenuhnya dummy**, dibuat dengan `numpy` dan `pandas` untuk keperluan eksplorasi awal.  

## Arsitektur Sistem
Alur sistem prediksi:  
Input data anggota → Preprocessing (One-Hot Encoding) → Model Logistic Regression → Output prediksi (Aktif / Tidak Aktif)

## Struktur Repository
- `README.md` → dokumentasi utama proyek  
- `notebooks/` → notebook eksplorasi dataset dummy  
- `src/` → kode model machine learning  
- `data/` → dataset dummy  
- `docs/` → dokumentasi tambahan  
- `issues board` → manajemen To Do / In Progress / Done (≥5 issue)

## Issue Board
### To Do
- [ ] Definisikan kebutuhan & problem UKM  
- [ ] Buat dataset dummy (anggota UKM)  
- [ ] Preprocessing data (encoding kategorikal)  
- [ ] Implementasi Logistic Regression  
- [ ] Buat evaluasi baseline dengan F1-Score  

### In Progress
- [ ] Dokumentasi hasil eksperimen  

### Done
- [x] Setup repository & struktur folder  
- [x] Inisialisasi README.md  

## Roadmap
- M1: Definisi masalah & setup repositori  
- M2: Pembuatan dataset dummy anggota UKM  
- M3: Preprocessing data (One-Hot Encoding)  
- M4: Implementasi model Logistic Regression  
- M5: Evaluasi F1-Score & analisis hasil  
- M6: Dokumentasi & laporan akhir  

## Etika & Privasi
**Risiko:** penggunaan data mahasiswa asli bisa menimbulkan masalah privasi dan penyalahgunaan informasi.  
**Mitigasi:** dalam proyek ini hanya digunakan **dummy dataset**, sehingga tidak ada data pribadi mahasiswa yang terlibat. Jika nantinya menggunakan data riil, perlu izin resmi, anonimisasi data, dan kontrol akses ketat untuk menjaga privasi.
