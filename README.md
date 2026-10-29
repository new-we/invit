# Undangan Pernikahan — Hendi & Istiq

Tema dasar: Melati, dibuat se-premium mungkin (hijau zamrud + emas + ivory, bingkai emas ganda, foto lengkung, kelopak melati jatuh, countdown live).

## Data yang dipakai (sesuai formulir)
- Mempelai pria: Hendi Krisdianto (Hendi), putra ke-1 Bapak Ngatolah & Ibu Sulis Indayani, Kraton Yosowilangun Lumajang
- Mempelai wanita: Istiq Lailatul Mukaromah (Istiq), putri ke-1 Bapak Khasbullah & Ibu Siti Mujayanah, Ngampelrejo Jombang Jember
- Akad: Minggu, 6 Desember 2026, 09.00 WIB, kediaman mempelai wanita, Ngampelrejo Jombang Jember
- Resepsi: Minggu, 6 Desember 2026, waktu Bebas, lokasi yang sama
- RSVP WhatsApp: 082314559412
- Amplop digital: DANA 082314549412
- Nama tamu otomatis: tambahkan `?to=NamaTamu` di akhir URL, mis. `?to=Bapak%20Andi`

## Yang sengaja TIDAK dikarang
- Tidak ada kisah cinta / timeline pertemuan (tidak ada di formulir) — bagian itu tidak dimasukkan.
- Tidak ada ucapan contoh atas nama orang lain — kolom ucapan mulai kosong.
- Tidak ada nama pemilik rekening DANA (tidak ada di formulir) — hanya nomor yang tampil.
- Link peta memakai pencarian Google Maps "Ngampelrejo Jombang Jember", bukan pin titik persis, karena link Maps tidak dilampirkan di formulir.

## PERHATIKAN sebelum dibagikan
- Nomor RSVP (082314559412) dan nomor DANA (082314549412) BERBEDA satu digit — keduanya dipakai persis seperti di formulir. Mohon dicek ulang ke pengantin, jangan sampai salah satu tertukar.
- Kolom ucapan di halaman ini bersifat demo frontend-only (ucapan hilang saat refresh), sama seperti template demo Melati. Kalau mau ucapan tersimpan permanen, perlu backend — beri tahu MUMU.

## Menambah foto prewedding nanti
1. Simpan foto prewedding ke folder `img/` dengan nama `prewed-1.jpg`, `prewed-2.jpg`, dst.
2. Di `index.html`, cari komentar `<!-- PREWED-1 ... -->` di bagian Galeri.
3. Ganti kotak "Foto Prewedding Menyusul" dengan baris gambar, contoh:
   `<img src="./img/prewed-1.jpg" alt="Foto prewedding 1">`
   (atau tambahkan baris itu di dalam grid galeri bersama foto Hendi & Istiq).
4. Commit & redeploy — tidak perlu mengubah file lain.

## Deploy ke Cloudflare Pages
- Repo: `new-we/invit` (branch `main`, root).
- Framework preset: None. Build command: (kosong). Build output directory: `/` (root).
- File ini statis penuh (HTML + 2 foto di `img/`), tanpa build step dan tanpa backend.
