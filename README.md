# APK Kasir — Cafe 500 & Scoot POS

Dua aplikasi Android dari satu proyek, masing-masing dengan berkas dan cara
pasangnya sendiri:

- **Cafe 500 Kasir** — POS genggam Cafe 500 (`order.cafe500.id/staff`).
- **Scoot POS** — tablet kasir Scoot Fitness (`app.scootactive.com/pos`).

---

## Cafe 500 Kasir

Aplikasi kasir Cafe 500 untuk POS genggam **Kassen XA-02 Pro** (ODM Ciontek;
sistemnya melapor *Ciontek CS30*, Android 11): pembungkus layar staf
`order.cafe500.id/staff`, portrait, cetak struk 58mm lewat printer bawaan.

### Berkas

| Berkas | Versi | Catatan |
|---|---|---|
| `cafe500-kasir-1.4.apk` | 1.4 (versionCode 5) | **Terbaru — pakai ini.** Logo Cafe 500 di struk (sebelumnya logo Scoot ikut tercetak) dan nomor antrean dicetak besar sebagai gambar. Ditandatangani **kunci rilis BARU (2026-09-19)** — lihat peringatan di bawah. |
| `cafe500-kasir-1.3.apk` | 1.3 (versionCode 4) | Lama. Printer bawaan, tampilan staf baru, auto-update. Kunci rilis lama. |
| `cafe500-kasir-1.1-debug.apk` | 1.1 (versionCode 2) | Lama. Hanya menambah Diagnosa servis sistem; belum bisa mencetak lewat printer bawaan. |
| `cafe500-kasir-1.0-debug.apk` | 1.0 (versionCode 1) | Lama. Disimpan sebagai arsip. |

**Cek keaslian 1.4** (opsional):
- SHA-256 berkas: `694b244a52eb2c3318d2f5655b8793d37f8ebc456637b8af43b7831ef08f31c7`
- Sertifikat penanda tangan (SHA-256): `0599d62057f7a03641837292845310b33e6d78c1dbf0e16137f078a6559bb360`
  — cek dengan `apksigner verify --print-certs cafe500-kasir-1.4.apk`.
  (1.3 memakai sertifikat lama `314dec90…62dcb9d0`.)

### Pasang 1.4 (sekali — juga dari 1.3)

> ⚠️ **1.4 memakai kunci rilis yang BERBEDA dari 1.3** (kunci dibuat ulang
> 2026-09-19). Android menolak memasangnya di atas 1.3 ("App not installed"),
> dan spanduk pembaruan otomatis di 1.3 juga tidak bisa memasangnya. **Uninstall
> dulu** Cafe 500 Kasir yang terpasang. Uninstall menghapus sesi login — siapkan
> akun kasir. Sesudah 1.4 terpasang, versi berikutnya kembali otomatis.

1. Setelan → Apps → **Cafe 500 Kasir** → **Uninstall**.
2. Izinkan **Install dari sumber tidak dikenal** untuk aplikasi yang dipakai
   mengunduh (browser / pengelola berkas).
3. Unduh `cafe500-kasir-1.4.apk`, ketuk → **Install**. Bila Play Protect
   memblokir: **Detail selengkapnya** → **Tetap instal**.
4. Buka aplikasi → login akun kasir kafe.
5. Uji printer: buka struk pesanan mana saja → **Pilih Printer** → **Tes cetak**.
   Struk uji memuat penggaris 32 karakter (bila muat satu baris, lebar struk
   benar), logo Cafe 500, dan contoh nomor antrean `88` berukuran besar.

### Pembaruan berikutnya (otomatis)

Mulai 1.4 tidak perlu mengunduh dari sini lagi. Saat versi baru dirilis, aplikasi
menampilkan banner **"Versi X tersedia" → Pasang**:

1. Ketuk **Pasang**. Pertama kali, Android meminta izin **"Pasang aplikasi tak
   dikenal"** untuk Cafe 500 Kasir — izinkan, lalu ketuk **Pasang** lagi.
2. Konfirmasi **Install** di dialog Android. Data & login tetap (tanpa uninstall).

Periksa manual kapan saja: tab **Lainnya → Periksa pembaruan aplikasi**.

### Kalau struk tidak tercetak

1. Buka struk → **Pilih Printer** → **Tes cetak**. Pesan gagal menyebut sebabnya
   (mis. kertas habis).
2. Masih gagal → **Diagnosa printer** → **Bagikan**, kirim teksnya ke yang
   menangani aplikasi. Diagnosa hanya membaca; ia tidak mencetak apa pun.

---

## Scoot POS (tablet kasir gym)

Aplikasi kasir Scoot Fitness untuk **tablet konter** (landscape): pembungkus
`app.scootactive.com/pos`, cetak struk 58mm lewat **printer Bluetooth**, plus
agen sinkron wajah ke mesin pintu Hikvision (diatur admin dari menu
*Wajah di Pintu*).

### Berkas

| Berkas | Versi | Catatan |
|---|---|---|
| `scoot-pos-1.8.1.apk` | 1.8.1 (versionCode 10) | **Terbaru — pakai ini.** Sama dengan 1.8 + IP mesin Hikvision cabang yang asli (1.8 menolak IP mesin di tombol "Tes koneksi"). Kunci rilis yang sama dengan 1.8: dari 1.8 cukup lewat spanduk pembaruan, tanpa uninstall. |
| `scoot-pos-1.8.apk` | 1.8 (versionCode 9) | Rilis **kunci rilis** pertama untuk gym (versi ≤ 1.7 = kunci debug). Layar setelan agen wajah terbaca, nomor antrean struk kafe tercetak besar, auto-update. IP mesin masih contoh. |

**Cek keaslian 1.8.1** (opsional):
- SHA-256 berkas: `19b5852604ec584c11529ff8cb1fbfc3bf57a1bd3371210b62eb67b38b7b682f`
  (1.8: `8350b439d4958ebb584e1086fe0b8011ac05210e4330f88126d9b493d2ffabe6`)
- Sertifikat penanda tangan (SHA-256): `e7fb5cc59253d84b741ba4ff9fc4b9dfd597a960b074d562b169f1b67a0cc1ea`
  — cek dengan `apksigner verify --print-certs scoot-pos-1.8.1.apk`.

### Pasang 1.8.1 (sekali, dari versi lama)

> ⚠️ **1.8.x memakai kunci rilis yang BERBEDA dari semua versi sebelumnya**
> (≤ 1.7 ditandatangani kunci debug laptop pembangun). Android menolak
> memasangnya di atas aplikasi lama ("App not installed"). **Uninstall dulu**
> Scoot POS yang lama. Yang hilang saat uninstall: sesi login, pilihan printer
> Bluetooth, dan seluruh setelan agen wajah (bila sudah pernah diisi) — catat
> dulu, isi ulang sesudahnya.

1. Lepas sematan layar (screen pinning) bila aktif, lalu Setelan → Apps →
   **Scoot POS** → **Uninstall**.
2. Izinkan **Install dari sumber tidak dikenal** untuk aplikasi yang dipakai
   mengunduh (browser / pengelola berkas).
3. Unduh `scoot-pos-1.8.1.apk`, ketuk → **Install**. Bila Play Protect memblokir:
   **Detail selengkapnya** → **Tetap instal**.
4. Buka aplikasi → login akun kasir/admin.
5. Struk → **Pilih Printer** → pilih printer Bluetooth yang sudah dipasangkan →
   cetak satu struk untuk uji.
6. (Admin, bila cabang memakai mesin wajah) menu **Wajah di Pintu** →
   **Pengaturan Agen (tablet ini)** → isi cabang, token, IP mesin, user/password
   mesin → **Tes koneksi & kalibrasi** → nyalakan **Agen aktif** → Simpan →
   tekan **Kecualikan dari optimasi baterai**. Bila tombol Tes menolak IP-nya
   ("tidak termasuk"), APK-nya perlu dibangun ulang dengan IP mesin cabang itu —
   hubungi yang menangani aplikasi.
7. Sematkan layar lagi.

### Pembaruan berikutnya (otomatis)

Mulai 1.8.x tidak perlu mengunduh dari sini lagi. Saat versi baru dirilis, layar
POS menampilkan banner **"Versi X tersedia" → Pasang**; pertama kali Android
meminta izin **"Pasang aplikasi tak dikenal"** untuk Scoot POS — izinkan, ketuk
**Pasang** lagi, lalu **Install**. Data, login, printer, dan setelan agen tetap
(tanpa uninstall). Bila tablet disematkan dan dialog pemasangan tidak muncul,
lepas sematan dulu lalu ketuk **Pasang** lagi.

Periksa manual kapan saja: menu pengguna (pojok kanan atas) →
**Periksa pembaruan aplikasi**.
