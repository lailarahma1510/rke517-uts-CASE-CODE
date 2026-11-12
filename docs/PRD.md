# Mini-PRD: CASE-CODE

Anything the client did not say is labelled **(my assumption)**.

## 1. Problem and goal
Masalah: 
Bulan lalu terdapat 46 klaim BPJS yang pending karena ada halaman berkas yang hilang. Selain itu, pencatatan masih manual/Excel terpecah di 3 komputer, dan kedisiplinan pengiriman berkas dari bangsal melewati batas waktu 3 hari (SPO RM-54).
Tujuan (Goal):
- Membuat aplikasi/sistem pengecekan kelengkapan berkas klaim BPJS secara digital agar Bapak Dedi Kurniawan dapat memantau status setiap kasus secara real-time tanpa harus bertanya ke staf.
- Menyediakan layar/antarmuka khusus bagi perawat bangsal (ward nurse) untuk melihat daftar berkas yang dikembalikan (retur) beserta alasan pengembaliannya secara real-time.
## 2. Users and scope
| User | What they do in the app |
|---|---|
| Claims Officer (Mas Andi) | Memeriksa kelengkapan berkas klaim (SEP, resume medis, lab, billing) dan memperbarui status berkas. |
| Ward Nurse | Mengirimkan folder berkas dari bangsal serta memastikan kepatuhan batas waktu pengiriman 3 hari. |
| Finance Officer (Bapak Dedi) | Memantau status rekapitulasi klaim secara real-time untuk mencegah klaim pending. |
Ward Nurse | Mengirimkan folder berkas dari bangsal, memastikan kepatuhan batas waktu pengiriman 3 hari, serta memantau layar status berkas yang dikembalikan beserta alasannya.
**IN:** Berkas klaim BPJS masuk dari bangsal (SEP, resume medis bertanda tangan DPJP, hasil lab, billing).
**OUT:** Status kelengkapan berkas, laporan rekapitulasi klaim harian/bulanan, dan notifikasi keterlambatan bangsal.

## 3. User stories
- **US-1** As a claims officer, I want to digitally check the completeness of SEP, discharge resume, lab results, and billing, so that no pages are missing before submission.
- **US-2** As a finance officer, I want to track the status of all claim files and monitor ward submission delays, so that I can see the status at any time without asking anyone.

## 4. Checks (Situation, Action, Result)
| ID | Story | Situation | Action | Result |
|---|---|---|---|---|
| C-1 | US-1 | Berkas klaim dikirim dari bangsal dengan resume medis belum ditandatangani DPJP | Petugas klaim memeriksa dan sistem mendeteksi tanda tangan kosong | Status otomatis menjadi "Returned" (dikembalikan ke bangsal) |
| C-2 | US-2 | Berkas dikirim melewati batas waktu 3 hari setelah pasien pulang | Sistem mencatat tanggal keluar dan tanggal terima dari bangsal | Sistem merekapitulasi keterlambatan bangsal secara real-time |

## 5. Data list
| Data item | Example | Who enters it | Required? | Kept in (entity) |
|---|---|---|---|---|
| Nomor SEP | 0301R0011125V000123 | Claims Officer | Yes | Claim Database |
| Nomor RM | 44-21-09 | Claims Officer | Yes | Claim Database |
| Nama Pasien | Rahmat | Claims Officer | Yes | Claim Database |
| Tanggal Keluar (Discharged) | 02/11/2026 | Ward Nurse | Yes | Claim Database |
| Status Resume Medis | Yes / No | Claims Officer | Yes | Claim Database |

## 6. Open questions
- Apakah sistem notifikasi keterlambatan pengiriman berkas dari bangsal perlu dikirim langsung via WhatsApp ke kepala ruangan?
- Bagaimana integrasi aplikasi ceklis ini dengan sistem SIMRS eksisting di RS Islam Al-Hikmah?
