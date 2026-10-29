# Undangan Pernikahan — Hendi & Istiq (v2, template Melati asli)

v2 ini = file template Melati asli (`undangan-demo/melati/index.html`) dengan HANYA datanya diganti.
Desain, warna (teal + beige + krem), cover gebyok/pohon/bunga, animasi, dan strukturnya persis Melati.
v1 (desain baru hijau zamrud + emas) DIGANTI oleh v2 ini atas permintaan kakak.

## Data yang dipakai (sesuai formulir)
- Mempelai pria: Hendi Krisdianto (Hendi), putra ke-1 Bapak Ngatolah & Ibu Sulis Indayani, Kraton Yosowilangun Lumajang
- Mempelai wanita: Istiq Lailatul Mukaromah (Istiq), putri ke-1 Bapak Khasbullah & Ibu Siti Mujayanah, Ngampelrejo Jombang Jember
- Akad: Minggu, 6 Desember 2026, 09.00 WIB, kediaman mempelai wanita, Ngampelrejo Jombang Jember
- Resepsi: Minggu, 6 Desember 2026, waktu Bebas, lokasi yang sama
- RSVP WhatsApp: 082314559412
- Amplop digital: DANA 082314549412
- Nama tamu otomatis: tambahkan `?to=NamaTamu` di akhir URL

## File di repo `new-we/invit` (branch main)
- `index.html` (root) — halaman undangan
- `README.md` (root) — file ini
- `img/hendi.jpg`, `img/istiq.jpg` — foto mempelai
- `img/bg-kebun.jpg`, `img/bunga-goyang.jpg`, `img/gebyok.jpg`, `img/pohon.jpg` — aset dekorasi template Melati (wajib ada, dipakai CSS/cover)

## Kredit pembuat
- Baris footer paling bawah: "Undangan Digital by Aditya Apps" (nama bisnis tertaut ke Instagram @aditya_apps).

## PERHATIKAN sebelum dibagikan
1. Bagian "Love Story" masih TEKS TEMPLATE Melati (pertemuan 2019, menjalin kasih 2021, lamaran 2026, menuju pernikahan 2027) karena kisah asli pasangan tidak ada di formulir. Ganti dulu dengan kisah asli mereka, atau hapus bagian itu, sebelum undangan dibagikan — jangan sampai klien mengira itu kisah mereka.
2. Nomor RSVP (082314559412) dan nomor DANA (082314549412) BERBEDA satu digit — keduanya dipakai persis seperti di formulir. Cek ulang ke pengantin.
3. Link peta memakai pencarian Google Maps "Ngampelrejo Jombang Jember", bukan pin titik persis (link Maps tidak dilampirkan di formulir).
4. Kolom ucapan bersifat demo frontend-only (ucapan hilang saat refresh), sama seperti template Melati.
5. Tidak ada nama pemilik rekening DANA di halaman (tidak ada di formulir).

## Menambah foto prewedding nanti
1. Simpan foto ke folder `img/` dengan nama `prewed-1.jpg`, `prewed-2.jpg`, dst.
2. Di `index.html`, cari komentar `<!-- PREWED ... -->` di bagian Galeri.
3. Ganti kotak "Foto Prewedding Menyusul" dengan baris gambar, contoh:
   `<img class="rv" data-a="zoom-out" src="./img/prewed-1.jpg" alt="Foto prewedding 1">`
4. Commit & redeploy — tidak perlu mengubah file lain.

## Deploy ke Cloudflare Pages
- Repo: `new-we/invit` (branch `main`, root).
- Framework preset: None. Build command: (kosong). Build output directory: `/` (root).
- Statis penuh, tanpa build step dan tanpa backend.

## Update: titik Maps & lagu
- Tombol "Lihat Peta" (akad & resepsi) memakai titik persis: https://maps.app.goo.gl/dbs9X9HSLiZSb9cn9
- Lagu: "Lagu Pernikahan Kita" — Tiara Andini & Arsy Widianto, diputar dari video resminya di YouTube (bukan file unduhan, jadi butuh internet). Lagu mulai otomatis saat tamu menekan "Buka Undangan", dari detik ke-102 (menit 1:42) dengan fade in 4 detik (volume naik pelan dari 0), lalu mengulang dari detik yang sama saat habis. Tombol musik bulat di pojok kanan bawah untuk jeda/lanjut.
- Menggeser posisi mulai lagu: ubah angka `MUSIC_START_SECONDS` di bagian script `index.html` (saat ini 102).
