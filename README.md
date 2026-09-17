# Cafe 500 Kasir — APK

Aplikasi kasir Cafe 500 untuk POS genggam **Kassen XA-02 Pro** (ODM Ciontek;
sistemnya melapor *Ciontek CS30*, Android 11): pembungkus layar staf
`order.cafe500.id/staff`, portrait, cetak struk 58mm lewat printer bawaan.

## Berkas

| Berkas | Versi | Catatan |
|---|---|---|
| `cafe500-kasir-1.3.apk` | 1.3 (versionCode 4) | **Terbaru — pakai ini.** Mencetak struk lewat **printer bawaan** mesin (tanpa Bluetooth), tampilan staf baru untuk layar HP (tab bar bawah: Papan · Kasir · Riwayat · Lainnya), dan **auto-update**. Ditandatangani **kunci rilis** (bukan kunci debug). |
| `cafe500-kasir-1.1-debug.apk` | 1.1 (versionCode 2) | Lama. Hanya menambah Diagnosa servis sistem; belum bisa mencetak lewat printer bawaan. |
| `cafe500-kasir-1.0-debug.apk` | 1.0 (versionCode 1) | Lama. Disimpan sebagai arsip. |

**Cek keaslian 1.3** (opsional):
- SHA-256 berkas: `ef8081dff81be0db928f469f9e79060121b76c6a585229d9c66c5ad400b5f158`
- Sertifikat penanda tangan (SHA-256): `314dec9051e769f97b4434026ebb913d9d85399ab6d7d34c1545885f62dcb9d0`
  — cek dengan `apksigner verify --print-certs cafe500-kasir-1.3.apk`.

## Pasang 1.3 (sekali, dari versi lama)

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

## Pembaruan berikutnya (otomatis)

Mulai 1.3 tidak perlu mengunduh dari sini lagi. Saat versi baru dirilis, aplikasi
menampilkan banner **"Versi X tersedia" → Pasang**:

1. Ketuk **Pasang**. Pertama kali, Android meminta izin **"Pasang aplikasi tak
   dikenal"** untuk Cafe 500 Kasir — izinkan, lalu ketuk **Pasang** lagi.
2. Konfirmasi **Install** di dialog Android. Data & login tetap (tanpa uninstall).

Periksa manual kapan saja: tab **Lainnya → Periksa pembaruan aplikasi**.

## Kalau struk tidak tercetak

1. Buka struk → **Pilih Printer** → **Tes cetak**. Pesan gagal menyebut sebabnya
   (mis. kertas habis).
2. Masih gagal → **Diagnosa printer** → **Bagikan**, kirim teksnya ke yang
   menangani aplikasi. Diagnosa hanya membaca; ia tidak mencetak apa pun.
