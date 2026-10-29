# Undangan Pernikahan — Hendi & Istiq (v2, template Melati asli)

v2 ini = file template Melati asli (`undangan-demo/melati/index.html`) dengan HANYA datanya diganti.
Desain, warna (teal + beige + krem), cover gebyok/pohon/bunga, animasi, dan strukturnya persis Melati.
v1 (desain baru hijau zamrud + emas) DIGANTI oleh v2 ini atas permintaan kakak.

## Data yang dipakai (sesuai formulir)
- Mempelai pria: Hendi Krisdianto (Hendi), putra ke-1 Bapak Ngatolah & Ibu Sulis Indayani, Kraton Yosowilangun Lumajang
- Mempelai wanita: Istiq Lailatul Mukaromah (Istiq), putri ke-1 Bapak Khasbullah & Ibu Siti Mujayanah, Ngampelrejo Jombang Jember
- Akad: Minggu, 6 Desember 2026, 09.00 WIB, kediaman mempelai wanita, Ngampelrejo Jombang Jember
- Resepsi: Minggu, 6 Desember 2026, waktu Bebas, lokasi yang sama
- RSVP WhatsApp: 082314549412 (sama dengan nomor DANA, koreksi 29 Okt — nomor lama 082314559412 SALAH)
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
1. Nomor RSVP dan nomor DANA SAMA (082314549412) — koreksi 29 Okt: nomor WA lama 082314559412 salah dan sudah diperbaiki di kedua tombol RSVP.
2. Link peta memakai pencarian Google Maps "Ngampelrejo Jombang Jember", bukan pin titik persis (link Maps tidak dilampirkan di formulir).
3. Kolom ucapan bersifat demo frontend-only (ucapan hilang saat refresh), sama seperti template Melati.
4. Tidak ada nama pemilik rekening DANA di halaman (tidak ada di formulir).

## Foto prewedding (SUDAH DITAMBAHKAN 29 Okt)
- Galeri kini berisi 3 foto prewedding: `img/prewed-1.jpg` (senja, gaun putih), `img/prewed-2.jpg` (taman, gaun hijau), `img/prewed-3.jpg` (formal, gaun biru) — ditambah foto Hendi & Istiq. Kotak "Foto Prewedding Menyusul" sudah dihapus.

## Deploy ke Cloudflare Pages
- Repo: `new-we/invit` (branch `main`, root).
- Framework preset: None. Build command: (kosong). Build output directory: `/` (root).
- Statis penuh, tanpa build step dan tanpa backend.

## Update: titik Maps & lagu
- Tombol "Lihat Peta" (akad & resepsi) memakai titik persis: https://maps.app.goo.gl/dbs9X9HSLiZSb9cn9
- Lagu: "Lagu Pernikahan Kita" — Tiara Andini & Arsy Widianto, diputar dari video resminya di YouTube (bukan file unduhan, jadi butuh internet). Lagu mulai otomatis saat tamu menekan "Buka Undangan", dari detik ke-102 (menit 1:42) dengan fade in 4 detik (volume naik pelan dari 0), lalu mengulang dari detik yang sama saat habis. Tombol musik bulat di pojok kanan bawah untuk jeda/lanjut.
- Menggeser posisi mulai lagu: ubah angka `MUSIC_START_SECONDS` di bagian script `index.html` (saat ini 102).

## Update: hilangkan putih & lembutkan pagar
- Penyebab kotak putih di awal buka: gambar dekorasi template aslinya JPG berlatar putih yang "disamarkan" dengan efek multiply — di HP efek itu sempat tidak jalan di detik awal, sehingga putihnya kelihatan. Perbaikan: latar putih ketiga gambar dekorasi (pohon, gebyok, bunga) benar-benar dihapus menjadi transparan (format WebP: pohon.webp, gebyok.webp, bunga-goyang.webp), dan efek multiply dihapus. Sekarang tidak ada lagi kotak putih, kapan pun gambarnya muncul.
- Kartu cover: animasi gesernya menimpa posisi tengah kartu sehingga kartu sempat muncul dari pojok kanan bawah lalu loncat ke tengah. Perbaikan: kartu sekarang langsung di tengah sejak awal dan hanya fade in (opacity saja).
- Pagar ukir (gebyok): dibuat lebih menyatu dengan latar lewat opacity 0,62, jadi cokelat tuanya tidak terlalu kontras.
- File JPG dekorasi lama di repo tidak dipakai lagi oleh halaman (halaman memakai WebP), tapi dibiarkan di repo agar tidak merusak apa pun.

## Update: semua fade in kalem
- Cover: latar, pagar, pohon, dan bunga tidak lagi geser/zoom — semuanya fade in pelan (opacity saja, 2,5–3 detik, bertahap): latar dulu, lalu pagar & bunga, terakhir bingkai tengah (kartu) mulai detik 1,2 selama 2,8 detik. Goyangan bunga tetap ada setelah muncul, tapi tidak lagi kasar di awal.
- Isi undangan saat di-scroll juga dilembutkan: naiknya hanya 16px (sebelumnya 40px) selama 1,6 detik, dan zoom-nya hanya dari 1,08x (sebelumnya 1,25x) selama 1,8 detik.

## Love Story (SUDAH DIISI KISAH ASLI 29 Okt)
- Pertemuan Pertama 2024, Menjalin Kasih 2025, Lamaran 2026, Pernikahan 2026 — kisahnya dari pengantin, kata-katanya diromantiskan (atas permintaan kakak 29 Okt), bukan lagi teks template.

## Update: pagar langsung menyatu sejak awal
- Penyebab keluhan: pagar tadinya fade menuju opacity 1 lalu mendadak kembali ke 0,62 setelah animasi selesai, sehingga sempat terlihat kontras lalu berubah. Perbaikan: pagar kini fade langsung menuju 0,62 dan bertahan di sana (keyframes fadeGeb), jadi sejak pertama muncul sudah menyatu, tidak ada lagi perubahan mendadak.

## Update: kartu mempelai sejajar
- Foto digeser agak ke atas (padding atas kartu dikecilkan) supaya kartu tidak terlalu penuh, dan foto sedikit digeser ke atas di dalam bingkai oval.
- Nama dibuat sejajar: blok nama diberi tinggi minimum setara 3 baris, sehingga "Putra ke-1 dari" dan "Putri ke-1 dari" selalu mulai di garis yang sama meski jumlah baris nama berbeda. Terverifikasi lewat screenshot lokal: foto sejajar, nama sejajar, keterangan sejajar.
