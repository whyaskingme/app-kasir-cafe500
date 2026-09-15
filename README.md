# Cafe 500 Kasir — APK

Aplikasi kasir Cafe 500 untuk mesin POS Android (pembungkus layar staf
`order.cafe500.id/staff`, portrait, cetak struk 58mm).

## Berkas

| Berkas | Versi | Catatan |
|---|---|---|
| `cafe500-kasir-1.1-debug.apk` | 1.1 (versionCode 2) | **Terbaru.** Tombol **Diagnosa printer** kini juga memeriksa **servis sistem** perangkat, bukan cuma aplikasi terpasang / port serial / USB / Bluetooth. Diperlukan untuk mesin ber-ODM Ciontek (mis. Kassen XA-02 Pro), yang printer bawaannya tidak muncul di keempat pemeriksaan lama. |
| `cafe500-kasir-1.0-debug.apk` | 1.0 (versionCode 1) | Versi sebelumnya. Disimpan sebagai cadangan. |

**Belum ada driver printer bawaan di kedua versi.** Mencetak bekerja lewat
printer Bluetooth yang dipasangkan (termasuk printer internal yang tampil
sebagai perangkat Bluetooth). Versi 1.1 adalah alat untuk memastikan jalur mana
yang tersedia di mesin Anda.

## Pasang

1. Setelan → izinkan **Install dari sumber tidak dikenal**.
2. Unduh APK di atas, ketuk → **Install**.

> ⚠️ **1.0 dan 1.1 ditandatangani kunci debug yang BERBEDA.** Android akan
> menolak memasang 1.1 di atas 1.0 ("App not installed"). **Uninstall dulu**
> aplikasi lamanya, lalu pasang 1.1. Setelan printer (MAC Bluetooth) ikut
> terhapus dan perlu dipilih ulang.

## Kalau struk tidak tercetak

1. Buka aplikasi → dialog **Pilih Printer**.
2. Printer muncul di daftar → pilih, selesai.
3. Tidak muncul → ketuk **Diagnosa printer** → **Bagikan**, kirim teksnya ke
   yang menangani aplikasi. Diagnosa hanya membaca; ia tidak mengirim perintah
   apa pun ke printer.
