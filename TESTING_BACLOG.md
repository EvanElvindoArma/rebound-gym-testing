# Testing Backlog: Sistem Manajemen Membership Rebound Gym Jambi


Backlog ini memuat 12 pekerjaan pengujian: 2 selesai, 1 sedang berjalan, dan 9 belum dimulai.

| ID | Task | Owner | Priority | Status | Evidence |
| --- | --- | --- | --- | --- | --- |
| BL-01 | Finalisasi project charter (isi nama, NIM, nomor kelompok, dan tanggal) | \[Koordinator\] | HIGH | DONE | [00_Project_Charter] |
| BL-02 | Susun test plan | \[Test Planner / QA\] | HIGH | DONE | [01_Test_Plan] |
| BL-03 | Catat defect awal dari hasil FAIL (DEF-001 sampai DEF-004) | \[Tester\] | HIGH | DONE | 05\_Defect\_Log/DEFECT\_LOG |
| BL-04 | Siapkan lingkungan: impor database.sql dan jalankan aplikasi di localhost | \[Developer / Fix Owner\] | HIGH | TO DO | Catatan setup di 07\_Implementation/ |
| BL-05 | Siapkan data uji (akun member dan admin) | \[Developer / Fix Owner\] | HIGH | TO DO | 03\_Test\_Data/ |
| BL-06 | Eksekusi ulang test case positive (TC-P-01 sampai TC-P-05) dengan screenshot | \[Anggota A\] | HIGH | TO DO | [04_Execution_Evidence] |
| BL-07 | Eksekusi ulang test case negative (TC-N-01 sampai TC-N-05) dengan screenshot | \[Anggota B\] | HIGH | TO DO | [04_Execution_Evidence] |
| BL-08 | Eksekusi ulang test case edge (TC-E-01 sampai TC-E-05) dengan screenshot | \[Anggota C\] | HIGH | TO DO | [04_Execution_Evidence] |
| BL-09 | Verifikasi ulang DEF-002 (data uji password dengan spasi) | \[Anggota C\] | MEDIUM | TO DO | 05\_Defect\_Log/ |
| BL-10 | Konfirmasi form yang diuji pada DEF-003 dan DEF-004 (pendaftaran mandiri atau tambah member oleh admin) | \[Anggota C\] | MEDIUM | TO DO | [05_Defect_Log] |
| BL-11 | Review test plan dan hasil eksekusi (naik ke v0.2) | \[Reviewer\] | MEDIUM | TO DO | 01\_Test\_Plan/ |
| BL-12 | Susun laporan hasil analisis dan testing | \[Documentation\] | MEDIUM | TO DO | 06\_Test\_Report/ |

## Aturan Backlog

- Satu tugas, satu owner, satu status.
- Status yang dipakai: TO DO, IN PROGRESS, dan DONE. Sebuah tugas baru boleh DONE bila buktinya sudah tersimpan di folder pada kolom Evidence.
- Priority: HIGH untuk pekerjaan yang menghalangi pengujian atau menjadi syarat selesai, MEDIUM untuk pekerjaan pendukung.
- Backlog diperbarui setelah setiap eksekusi test case, review, atau perubahan test plan, oleh owner tugas yang bersangkutan.
