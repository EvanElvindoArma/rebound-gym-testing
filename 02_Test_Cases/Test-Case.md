## 6. Test Case dan Owner

| ID | Kategori | Skenario | Data Uji | Hasil Diharapkan | Owner | Status Awal |
| --- | --- | --- | --- | --- | --- | --- |
| TC-P-01 | Positive | Login member dengan data valid | Email dan password valid | Masuk ke dashboard member | Bel kalinton | PASS |
| TC-P-02 | Positive | Login admin dengan data valid | Email dan password admin valid | Masuk ke dashboard admin | Bel kalinton | PASS |
| TC-P-03 | Positive | Daftar akun baru | Nama lengkap, email, no. HP, alamat, password | Pendaftaran berhasil dan diarahkan ke halaman login | Bel Kalinton | PASS |
| TC-P-04 | Positive | Admin menambah paket membership | Paket Basic 1 Bulan | Paket bertambah dan muncul di riwayat membership | Bel Kalinton | PASS |
| TC-P-05 | Positive | Admin menghapus atau mengedit paket | Pilih paket, hapus, konfirmasi OK | Paket terhapus atau berubah dan tampilan langsung diperbarui | Bel Kalinton | PASS |
| TC-N-01 | Negative | Admin menambah member dengan field kosong | Semua field kosong | Validasi gagal dan pesan 'Harap isi bidang ini' muncul | Ella Elvira | PASS |
| TC-N-02 | Negative | Login dengan akun salah | Email atau password salah | Login gagal dan pesan error muncul | Ella Elvira | PASS |
| TC-N-03 | Negative | Login dengan field kosong | Email dan password kosong | Validasi gagal dan pesan 'Harap isi bidang ini' muncul | Ella Elvira | PASS |
| TC-N-04 | Negative | Harga paket diisi huruf | Lima Ribu Rupiah | Sistem menolak input | Ella Elvira | PASS |
| TC-N-05 | Negative | Nomor diisi non-angka | nur | Sistem memberi peringatan | Ella Elvira | PASS |
| TC-E-01 | Edge | Nama dengan karakter panjang | abcdefghkforugjbbbbbbb | Sistem menolak nama yang panjang | Echa Ramandha | FAIL |
| TC-E-02 | Edge | Password dengan spasi | password123 | Sistem memproses dengan benar | Echa Ramandha | FAIL |
| TC-E-03 | Edge | Nomor WhatsApp berisi huruf | 0812-abc-def | Sistem menolak input | Echa Ramandha | FAIL |
| TC-E-04 | Edge | Pendaftaran dengan email yang sama | Email yang sudah terdaftar | Sistem menolak email yang sama | Echa Ramandha | PASS |
| TC-E-05 | Edge | Password kurang dari 6 karakter | 12345 | Sistem memberi peringatan | Echa Ramandha | FAIL |
