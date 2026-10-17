# Struktur Repository dan Aturan Versioning: Rebound Gym Jambi


Repository menjadi tempat bersama untuk dokumen, bukti, dan catatan pengujian, dengan target orang lain dapat memahami proyek tanpa bertanya dari awal.

## 1. Struktur Folder

```
REBOUND-GYM-TESTING/
├── 00_Project_Charter/
├── 01_Test_Plan/
├── 02_Test_Cases/
├── 03_Test_Data/
├── 04_Execution_Evidence/
├── 05_Defect_Log/
├── 06_Test_Report/
├── 07_Implementation/
├── TESTING_BACKLOG
├── REPOSITORY_GUIDE
└── README.md
```

| Folder | Isi | PIC |
| --- | --- | --- |
| 00\_Project\_Charter | Project charter dan revisinya | \[Koordinator\] |
| 01\_Test\_Plan | TEST\_PLAN dan versinya | \[Test Planner / QA\] |
| 02\_Test\_Cases | Lembar skenario 15 test case beserta hasil aktual | \[Test Planner / QA\] dan \[Tester\] |
| 03\_Test\_Data | Data uji per test case dan akun uji | \[Developer / Fix Owner\] |
| 04\_Execution\_Evidence | Screenshot hasil eksekusi per test case | \[Tester\] |
| 05\_Defect\_Log | DEFECT\_LOG dan bukti tiap defect | \[Tester\] |
| 06\_Test\_Report | Laporan hasil analisis dan testing | \[Documentation\] |
| 07\_Implementation | Arsip aplikasi rebound\_gym yang diuji dan catatan setup lingkungan | \[Developer / Fix Owner\] |
| README.md | Daftar isi, pembagian tugas, dan tautan ke dokumen aktif | \[Documentation\] |

Folder 00\_Project\_Charter ditambahkan karena struktur dasar dari slide tidak memiliki tempat untuk charter. Semua anggota dapat membaca seluruh folder, dan isi tiap folder diperbarui oleh PIC-nya.

Dokumen kerja TESTING\_BACKLOG dan REPOSITORY\_GUIDE ditaruh di folder utama, berdampingan dengan README.md, karena keduanya tidak memiliki folder khusus. Status terbaru pekerjaan selalu dilihat di TESTING\_BACKLOG.

## 2. Aturan Penamaan File

Format dokumen: NAMA\_DOKUMEN\_vX.Y\[\_status\].ekstensi, dengan contoh berikut.

- TEST\_PLAN\_v0.1 untuk draf pertama.
- TEST\_PLAN\_v0.2\_review untuk versi yang sedang direview.
- TEST\_PLAN\_v1.0\_approved untuk versi yang sudah disetujui.

Format bukti: TC-E-01\_YYYYMMDD\_owner.png untuk test case, dan DEF-001\_YYYYMMDD.png untuk defect.

## 3. Aturan Versioning

| Versi | Status | Arti |
| --- | --- | --- |
| v0.1 | DRAFT | Draf pertama dari penyusun |
| v0.2 | REVIEW | Sedang diperiksa Reviewer |
| v0.3 | REVISED | Sudah direvisi sesuai hasil review |
| v1.0 | APPROVED | Disetujui Koordinator dan tidak diubah tanpa menaikkan versi |

- Gunakan penamaan versi yang konsisten dan hindari nama seperti final.docx, final2.docx, atau final\_baru.docx.
- Catat perubahan penting pada tabel riwayat versi di dalam setiap dokumen.
- Penyetuju versi final adalah \[Koordinator\], setelah Reviewer memeriksa.
- Versi lama tidak dihapus, tetapi dipindahkan ke subfolder \_archive di folder yang sama.
- Defect Log dan Testing Backlog adalah catatan hidup yang terus diperbarui. Riwayatnya mengikuti riwayat perubahan dokumennya, sehingga tidak diberi nomor versi.

## 4. Alur Kerja dan Komunikasi Defect

| Langkah | Siapa | Hasil dan bukti |
| --- | --- | --- |
| Plan | \[Test Planner / QA\] | Test plan diperbarui di 01\_Test\_Plan |
| Assign | \[Koordinator\] | Owner dan target waktu tercatat di Testing Backlog |
| Execute | \[Tester\] | Test case dijalankan sesuai test plan |
| Log | \[Tester\] | Screenshot di 04\_Execution\_Evidence dan defect di 05\_Defect\_Log |
| Review | \[Reviewer\] | Hasil dan bukti diperiksa, status defect dan versi dokumen diperbarui |
| Update | \[Documentation\] | Backlog, README, dan versi dokumen disinkronkan |

Defect dicatat di Defect Log lebih dulu, bukan lewat chat pribadi. Pesan ke Developer memuat ID defect, ID test case, langkah singkat, dan nama file bukti, misalnya: DEF-003 (TC-E-03) FAIL, nomor berisi huruf tersimpan, bukti di 04\_Execution\_Evidence. Developer / Fix Owner menganalisis, Tester melakukan retest bila ada perbaikan, dan Koordinator memastikan status terbaru.

## 5. Riwayat Versi

| Versi | Status | Perubahan | Penyusun |
| --- | --- | --- | --- |
| v0.1 | DRAFT | Draf awal struktur folder, penamaan, versioning, dan alur kerja | \[Documentation\] |
