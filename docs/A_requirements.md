# A. Understanding the client

## Problem and goal
**Problem:** Terjadi 46 klaim BPJS yang pending pada bulan lalu akibat halaman berkas yang hilang, pencatatan manual/Excel yang terpecah di 3 komputer, serta kedisiplinan pengiriman berkas dari bangsal yang melewati batas waktu 3 hari (SPO RM-54) dengan resume medis wajib ditandatangani DPJP.
**Goal:** Membangun sistem pengecekan dan pelacakan kelengkapan berkas klaim BPJS secara digital agar Finance and Claims Officer dapat memantau status secara real-time.

## Requirements
| ID | Requirement | Check: Situation | Action | Result | Source |
|---|---|---|---|---|---|
| R-01 | Sistem validasi kelengkapan dokumen klaim | Berkas klaim dari bangsal diterima dengan halaman resume medis kurang | Petugas klaim memasukkan data dan sistem mendeteksi dokumen kurang | Status berkas otomatis "Returned" (dikembalikan ke bangsal) | interview |
| R-02 | Monitoring keterlambatan pengiriman bangsal | Berkas dikirim melebihi batas waktu 3 hari setelah pasien keluar | Sistem mencatat tanggal keluar dan tanggal terima berkas | Sistem merekapitulasi daftar bangsal yang terlambat | form |

## Open questions
| ID | Question for the client | Why I ask (which sources disagree?) | My proposal until answered |
|---|---|---|---|
| Q-01 | Apakah validasi tanda tangan DPJP pada resume medis perlu menggunakan tanda tangan digital (e-signature)? | SOP internal rumah sakit belum merinci penggunaan tanda tangan digital secara penuh | Menggunakan status konfirmasi centang manual oleh petugas verifikasi |

