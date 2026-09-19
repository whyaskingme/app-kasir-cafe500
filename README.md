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
| `cafe500-kasir-1.3.apk` | 1.3 (versionCode 4) | **Terbaru — pakai ini.** Mencetak struk lewat **printer bawaan** mesin (tanpa Bluetooth), tampilan staf baru untuk layar HP (tab bar bawah: Papan · Kasir · Riwayat · Lainnya), dan **auto-update**. Ditandatangani **kunci rilis** (bukan kunci debug). |
| `cafe500-kasir-1.1-debug.apk` | 1.1 (versionCode 2) | Lama. Hanya menambah Diagnosa servis sistem; belum bisa mencetak lewat printer bawaan. |
| `cafe500-kasir-1.0-debug.apk` | 1.0 (versionCode 1) | Lama. Disimpan sebagai arsip. |

Versi 1.4 (logo Cafe 500 di struk + nomor antrean besar) menyusul lewat
pembaruan otomatis di dalam aplikasi — tidak perlu mengunduh dari sini.

**Cek keaslian 1.3** (opsional):
- SHA-256 berkas: `ef8081dff81be0db928f469f9e79060121b76c6a585229d9c66c5ad400b5f158`
- Sertifikat penanda tangan (SHA-256): `314dec9051e769f97b4434026ebb913d9d85399ab6d7d34c1545885f62dcb9d0`
  — cek dengan `apksigner verify --print-certs cafe500-kasir-1.3.apk`.

### Pasang 1.3 (sekali, dari versi lama)

> ⚠️ **1.3 memakai kunci rilis yang BERBEDA dari 1.0/1.1/1.2.** Android menolak
> memasangnya di atas aplikasi lama ("App not installed"). **Uninstall dulu**
> Cafe 500 Kasir yang lama. Uninstall menghapus sesi login — siapkan akun kasir.

1. Setelan → Apps → **Cafe 500 Kasir** → **Uninstall**.
2. Izinkan **Install dari sumber tidak dikenal** untuk aplikasi yang dipakai
   mengunduh (browser / pengelola berkas).
3. Unduh `cafe500-kasir-1.3.apk`, ketuk → **Install**. Bila Play Protect
   memblokir: **Detail selengkapnya** → **Tetap instal**.
4. Buka aplikasi → login akun kasir kafe.
5. Uji printer: buka struk pesanan mana saja → **Pilih Printer** → **Tes cetak**.
   Struk uji memuat penggaris 32 karakter — bila muat satu baris, lebar struk benar.

### Pembaruan berikutnya (otomatis)

Mulai 1.3 tidak perlu mengunduh dari sini lagi. Saat versi baru dirilis, aplikasi
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
| `scoot-pos-1.8.apk` | 1.8 (versionCode 9) | **Terbaru — pakai ini.** Rilis **kunci rilis** pertama untuk gym (versi ≤ 1.7 = kunci debug). Layar setelan agen wajah kini terbaca, nomor antrean struk kafe tercetak besar, dan **auto-update**. |

**Cek keaslian 1.8** (opsional):
- SHA-256 berkas: `8350b439d4958ebb584e1086fe0b8011ac05210e4330f88126d9b493d2ffabe6`
- Sertifikat penanda tangan (SHA-256): `e7fb5cc59253d84b741ba4ff9fc4b9dfd597a960b074d562b169f1b67a0cc1ea`
  — cek dengan `apksigner verify --print-certs scoot-pos-1.8.apk`.

### Pasang 1.8 (sekali, dari versi lama)

> ⚠️ **1.8 memakai kunci rilis yang BERBEDA dari semua versi sebelumnya**
> (≤ 1.7 ditandatangani kunci debug laptop pembangun). Android menolak
> memasangnya di atas aplikasi lama ("App not installed"). **Uninstall dulu**
> Scoot POS yang lama. Yang hilang saat uninstall: sesi login, pilihan printer
> Bluetooth, dan seluruh setelan agen wajah (bila sudah pernah diisi) — catat
> dulu, isi ulang sesudahnya.

1. Lepas sematan layar (screen pinning) bila aktif, lalu Setelan → Apps →
   **Scoot POS** → **Uninstall**.
2. Izinkan **Install dari sumber tidak dikenal** untuk aplikasi yang dipakai
   mengunduh (browser / pengelola berkas).
3. Unduh `scoot-pos-1.8.apk`, ketuk → **Install**. Bila Play Protect memblokir:
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

Mulai 1.8 tidak perlu mengunduh dari sini lagi. Saat versi baru dirilis, layar
POS menampilkan banner **"Versi X tersedia" → Pasang**; pertama kali Android
meminta izin **"Pasang aplikasi tak dikenal"** untuk Scoot POS — izinkan, ketuk
**Pasang** lagi, lalu **Install**. Data, login, printer, dan setelan agen tetap
(tanpa uninstall). Bila tablet disematkan dan dialog pemasangan tidak muncul,
lepas sematan dulu lalu ketuk **Pasang** lagi.

Periksa manual kapan saja: menu pengguna (pojok kanan atas) →
**Periksa pembaruan aplikasi**.
