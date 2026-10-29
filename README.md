# My Little Phone — simulasi iPhone untuk AU

Website statis untuk cerita fiksi/AU. Berjalan di browser HP dan dapat di-deploy ke Vercel.

## Fitur
- Lock screen dengan jam/tanggal dan kode sandi
- Home screen dengan ikon aplikasi
- Pesan dengan beberapa percakapan dan kirim pesan lokal
- Catatan yang tersimpan di browser
- Instagram dan X simulasi
- Foto, kalender, cuaca, telepon, Safari, pengaturan
- Layout responsif untuk HP

## Kode sandi
Kode awal adalah `1108`. Untuk mengganti, buka `script.js` lalu ubah:
```js
const PASSCODE = "1108";
```
Ini hanya kunci simulasi di sisi browser, bukan keamanan sungguhan.

## Cara deploy lewat Android
1. Unduh dan ekstrak ZIP ini.
2. Buka https://vercel.com lewat Chrome Android dan masuk/daftar.
3. Cara yang paling mudah: buka https://github.com, buat akun jika belum punya, lalu buat repository baru misalnya `my-little-phone`.
4. Unggah tiga file utama dari folder ini: `index.html`, `style.css`, dan `script.js` (bisa melalui browser GitHub dengan Add file → Upload files).
5. Di Vercel, pilih **Add New → Project**, hubungkan GitHub, lalu impor repository `my-little-phone`.
6. Karena ini website statis, biarkan Framework Preset sebagai **Other** (atau None), Build Command kosong, Output Directory kosong/default, lalu tekan **Deploy**.
7. Setelah selesai, Vercel memberi URL `.vercel.app`.

## Mengubah isi AU
- Pesan contoh: ubah objek `chats` di `script.js`.
- Nama aplikasi/isi aplikasi: ubah fungsi `renderApp()` di `script.js`.
- Foto wallpaper: cari `photo-bg` dan `blur-wallpaper` di `style.css`, lalu ganti URL gambar.
- Catatan: teks awal ada pada `notesText` di `script.js`.
- Password: ubah `PASSCODE`.

## Catatan
- Semua chat dan postingan adalah simulasi lokal, bukan terhubung ke WhatsApp/Instagram asli.
- Catatan tersimpan di browser yang sama melalui localStorage; jika data browser dihapus, catatan dapat hilang.
- Wallpaper contoh memakai gambar dari Unsplash sehingga memerlukan koneksi internet. Ganti dengan gambar milikmu bila ingin lebih personal.
