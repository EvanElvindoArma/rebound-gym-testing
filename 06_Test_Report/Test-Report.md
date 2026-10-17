# Test Report: Sistem Manajemen Membership Rebound Gym Jambi

Oct 17, 2026 · @EL

Dari 15 test case yang dieksekusi, 11 berstatus PASS dan 4 FAIL, dengan 4 defect tercatat yang seluruhnya masih OPEN.

## 1. Pendahuluan

Laporan ini merangkum hasil pengujian black-box/UAT pada sistem Rebound Gym Jambi, sebuah aplikasi web manajemen membership gym dengan hak akses member dan admin. Pengujian mengacu pada Project Charter, Test Plan v0.1, dan RTTM v0.1.

Scope pengujian mencakup autentikasi, validasi form, serta pengelolaan paket dan member oleh admin. Check-in, pembayaran, notifikasi, pembatasan akses antar-role, SQL injection dan XSS, serta load/stress tidak diuji.

## 2. Lingkungan Uji

| Komponen | Keterangan |
| --- | --- |
| Aplikasi | Rebound Gym Jambi (PHP native dan MySQL), arsip rebound\_gym |
| Database | MySQL rebound\_gym\_jambi, dibuat dari database.sql |
| Lingkungan | Localhost |
| Browser | \[sesuaikan\] |
| Data uji | DATA\_UJI\_v0.1 |
| Tanggal eksekusi | \[tanggal\] |
| Penguji | \[Nama\] |

## 3. Ringkasan Eksekusi

| Kategori | Jumlah | PASS | FAIL | Persentase PASS |
| --- | --- | --- | --- | --- |
| Positive | 5 | 5 | 0 | 100% |
| Negative | 5 | 5 | 0 | 100% |
| Edge case | 5 | 1 | 4 | 20% |
| Total | 15 | 11 | 4 | 73,3% |

## 4. Hasil per Requirement

Sebanyak 9 dari 12 requirement terpenuhi, dan 3 belum terpenuhi (R-08, R-09, dan R-10).

| Req ID | Requirement | Test ID | Hasil |
| --- | --- | --- | --- |
| R-01 | Login dengan kredensial valid | TC-P-01, TC-P-02 | Terpenuhi |
| R-02 | Login dengan kredensial salah atau kosong ditolak | TC-N-02, TC-N-03 | Terpenuhi |
| R-03 | Pendaftaran akun member baru | TC-P-03 | Terpenuhi |
| R-04 | Form tambah member menolak field wajib yang kosong | TC-N-01 | Terpenuhi |
| R-05 | Admin menambah paket membership | TC-P-04 | Terpenuhi |
| R-06 | Admin mengubah atau menghapus paket | TC-P-05 | Terpenuhi |
| R-07 | Harga paket hanya menerima angka | TC-N-04 | Terpenuhi |
| R-08 | Nomor WhatsApp hanya menerima angka | TC-N-05, TC-E-03 | Belum terpenuhi (DEF-003) |
| R-09 | Panjang nama dibatasi | TC-E-01 | Belum terpenuhi (DEF-001) |
| R-10 | Password minimal 6 karakter dan password yang memenuhi aturan diterima | TC-E-05, TC-E-02 | Belum terpenuhi (DEF-004, DEF-002) |
| R-11 | Email yang sudah terdaftar ditolak | TC-E-04 | Terpenuhi |
| R-12 | Pesan penolakan input jelas | TC-N-01, TC-N-03, TC-N-05 | Terpenuhi |

## 5. Ringkasan Defect

| ID | Test Case | Ringkasan | Severity | Status |
| --- | --- | --- | --- | --- |
| DEF-001 | TC-E-01 | Nama berkarakter panjang tetap diterima, dan batas panjang nama belum ditetapkan | LOW | OPEN |
| DEF-002 | TC-E-02 | Password password123 ditolak padahal diharapkan diterima; data uji tidak mengandung spasi sehingga perlu diverifikasi ulang | MEDIUM | OPEN |
| DEF-003 | TC-E-03 | Nomor WhatsApp berisi huruf tersimpan | MEDIUM | OPEN |
| DEF-004 | TC-E-05 | Password 5 karakter tetap diterima | MEDIUM | OPEN |

Severity merupakan usulan awal. Perbaikan kode berada di luar scope proyek, sehingga defect berhenti di status OPEN atau ASSIGNED beserta rekomendasi perbaikan.

## 6. Analisis

Seluruh test case positive dan negative berstatus PASS. Artinya alur utama (login, pendaftaran, dan pengelolaan paket) serta penolakan input dasar berjalan sesuai harapan.

Semua hasil FAIL berada pada edge case dan berkaitan dengan batas input: panjang nama, format nomor WhatsApp, dan panjang password. Pola ini menunjukkan validasi batas input belum konsisten di sistem.

Ada tiga catatan keterbatasan:

- Hasil PASS pada TC-N-01, TC-N-03, dan TC-N-04 kemungkinan berasal dari validasi browser, sehingga belum membuktikan bahwa server ikut memvalidasi input yang sama.
- DEF-002 perlu diverifikasi ulang karena data uji aslinya tidak mengandung spasi, padahal skenarionya adalah password dengan spasi.
- Area di luar scope (check-in, pembayaran, notifikasi, pembatasan akses, dan keamanan) belum diuji, sehingga hasil ini tidak menggambarkan kualitas sistem secara menyeluruh.

## 7. Kesimpulan dan Rekomendasi

Fitur inti sistem berfungsi pada skenario normal dan penolakan dasar, dengan 73,3% test case PASS. Namun validasi batas input belum memenuhi harapan, sehingga sistem belum dapat dinyatakan layak untuk input yang tidak terduga.

Rekomendasi:

1. Tetapkan dan terapkan batas panjang nama (DEF-001). Kolom nama di database menerima maksimal 150 karakter.
2. Validasi nomor WhatsApp agar hanya menerima angka di sisi server, pada semua form yang menerimanya (DEF-003).
3. Terapkan minimal 6 karakter untuk password pada semua form, termasuk tambah member oleh admin (DEF-004).
4. Verifikasi ulang DEF-002 dengan data yang benar-benar mengandung spasi, lalu tinjau aturan password (DEF-002).
5. Perluas pengujian ke area di luar scope pada tahap berikutnya.

## 8. Lampiran

- Dokumen terkait: Project Charter, Test Plan v0.1, RTTM v0.1, Defect Log, dan DATA\_UJI\_v0.1.
- Screenshot bukti pengujian: \[tautan atau folder 04\_Execution\_Evidence\].
