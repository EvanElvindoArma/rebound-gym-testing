# Analisis dan Testing Sistem Manajemen Membership Rebound Gym Jambi

Repository ini menyimpan dokumen, bukti, dan catatan pengujian untuk proyek mata kuliah **Testing dan Implementasi Sistem** (Kelas 5E), Program Studi Sistem Informasi, Fakultas Sains dan Teknologi, UIN Sulthan Thaha Saifuddin Jambi, tahun 2026.

**Kelompok:** [X]

Proyek ini menguji sistem Rebound Gym Jambi (PHP native dan MySQL) dengan pendekatan black-box/UAT: 15 test case yang terdiri dari 5 positive, 5 negative, dan 5 edge case.

## Anggota Tim

| Nama | NIM | Peran |
|---|---|---|
| [Adrian Aditia] | [701240151] | Koordinator / Leader |
| [Rifa Nadliaul Jannah] | [701240148] | Test Planner / QA |
| [Ella Elvira] | [701240134] | Tester |
| [Evan Elvindo Arma] | [701240143] | Developer / Fix Owner |
| [Bel Kalinton] | [701240151] | Reviewer |
| [Echa Ramandha] | [701240196] | Documentation |

## Struktur Repository

```
rebound-gym-testing/
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
|---|---|---|
| [00_Project_Charter](00_Project_Charter/) | Project charter dan revisinya | [Koordinator] |
| [01_Test_Plan](01_Test_Plan/) | Test plan dan versinya | [Test Planner / QA] |
| [02_Test_Cases](02_Test_Cases/) | Lembar skenario 15 test case beserta hasil aktual | [Test Planner / QA] dan [Tester] |
| [03_Test_Data](03_Test_Data/) | Data uji per test case dan akun uji | [Developer / Fix Owner] |
| [04_Execution_Evidence](04_Execution_Evidence/) | Screenshot hasil eksekusi per test case | [Tester] |
| [05_Defect_Log](05_Defect_Log/) | Defect log dan bukti tiap defect | [Tester] |
| [06_Test_Report](06_Test_Report/) | Laporan hasil analisis dan testing | [Documentation] |
| [07_Implementation](07_Implementation/) | Arsip aplikasi rebound_gym yang diuji dan catatan setup lingkungan | [Developer / Fix Owner] |

Di folder utama terdapat dua dokumen kerja: **TESTING_BACKLOG** (daftar pekerjaan, owner, priority, dan status) dan **REPOSITORY_GUIDE** (aturan penamaan, versioning, dan alur kerja). Status terbaru pekerjaan selalu dilihat di TESTING_BACKLOG.

## Aturan Singkat

- **Penamaan dokumen:** `NAMA_DOKUMEN_vX.Y[_status]`, misalnya `TEST_PLAN_v0.2_review`.
- **Versi:** v0.1 DRAFT, v0.2 REVIEW, v0.3 REVISED, v1.0 APPROVED. Versi final disetujui [Koordinator].
- **Bukti:** `TC-E-01_YYYYMMDD_owner.png` untuk test case dan `DEF-001_YYYYMMDD.png` untuk defect.
- **Defect:** dicatat lebih dulu di Defect Log, lalu dikomunikasikan ke Developer / Fix Owner dengan menyebut ID defect, ID test case, dan nama file bukti.
- **Pembaruan:** setiap perubahan di repository ditulis pada pesan commit yang menyebut dokumen dan perubahannya.

## Alur Kerja

Plan (Test Planner / QA) → Assign (Koordinator) → Execute (Tester) → Log (Tester) → Review (Reviewer) → Update (Documentation).