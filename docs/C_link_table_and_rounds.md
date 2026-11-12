# C. Link table and build plan

## Link table (one owner per data)
| Data | Owner (system or person) | Who reads it | How it moves |
|---|---|---|---|
| Data Klaim & SEP | Claims Officer (Mas Andi) | Finance Officer, Coder | Diinput manual dari berkas fisik ke sistem digital |
| Status Keterlambatan Bangsal | Ward Nurse | Claims Officer, Finance Officer | Dicatat otomatis berdasarkan tanggal keluar dan tanggal terima berkas |
| Status Kelengkapan Berkas | System | Finance Officer, Claims Officer | Diperbarui secara real-time saat verifikasi ceklis |

## Build plan in 3 rounds
| Round | What it delivers | What the client can check | What waits |
|---|---|---|---|
| 1 | Modul input data klaim dan ceklis kelengkapan dasar (SEP, resume medis) | Klien (Pak Dedi) dapat menguji input nomor SEP dan melihat status kelengkapan awal | Integrasi otomatis dengan sistem SIMRS rumah sakit |
| 2 | Modul pelacakan keterlambatan pengiriman berkas dari bangsal (SPO 3 hari) | Klien dapat memantau rekapitulasi keterlambatan pengiriman per bangsal | Fitur notifikasi otomatis via WhatsApp |
| 3 | Dashboard rekapitulasi klaim *real-time* dan laporan bulanan anti-pending | Klien dapat melihat laporan keseluruhan untuk mencegah 46 klaim *pending* | Penggunaan tanda tangan digital lanjutan untuk DPJP |
