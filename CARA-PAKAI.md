# Cara pakai website ulang tahun ini

Websitenya udah jalan penuh dari sekarang (opening → basa-basi → tiup lilin →
video → galeri foto → amplop surat). Yang belum ada cuma FILE MEDIA kamu sendiri.
Website ini sudah didesain supaya begitu kamu taruh file dengan NAMA yang tepat
di folder yang tepat, otomatis langsung muncul — nggak perlu edit kode sama sekali.

## 1. Video ucapan
Taruh 1 file video di:
```
assets/video/video.mp4
```
Format `.mp4` paling aman untuk semua browser.

Sekarang di paling awal ada pertanyaan "kamu buka ini pake apa? 📱 HP / 💻
Laptop". Berdasarkan jawaban itu, bingkai video otomatis berubah bentuk:
- Pilih **HP** → bingkai video jadi **portrait** (tegak, 9:16) — cocok kalau
  video kamu direkam vertikal ala story/reels.
- Pilih **Laptop** → bingkai video jadi **landscape** (mendatar, 16:9) —
  cocok kalau video kamu direkam horizontal.

Jadi idealnya siapkan video sesuai orientasi yang paling sering dipakai
Inesa (kalau nggak yakin, video portrait biasanya paling aman karena HP
tetap bisa nampilin landscape dengan sedikit ruang kosong).

Video akan otomatis coba autoplay dengan suara (karena user sudah banyak
berinteraksi sebelumnya lewat pertanyaan device, opening & tiup lilin).
Kalau browser tetap memblokir suara, ada tulisan kecil "ketuk video kalau
suaranya belum muncul" di bawah video — jadi tetap aman.

## 2. Lagu latar
Taruh 1 file lagu di:
```
assets/music/song.mp3
```
Lagu akan coba autoplay begitu masuk ke halaman utama. Ada tombol musik
bulat mengambang di pojok kanan bawah (♫) untuk nyala/mati kapan saja.

## 3. Foto-foto galeri
Ada **25 slot foto**, campuran potrait dan landscape, tiap foto agak miring
dikit (efek "ditempel scrapbook") dan posisinya zig-zag kiri-kanan otomatis.
Taruh foto dengan nama persis seperti ini di `assets/img/`:
```
assets/img/photo1.jpg
assets/img/photo2.jpg
...
assets/img/photo25.jpg
```
Selama belum ada file-nya, otomatis muncul kotak placeholder cantik
bertuliskan "taruh photo1.jpg di assets/img/" dst — jadi website tetap
kelihatan rapi meski belum diisi semua.

Beberapa foto sudah diatur sebagai **landscape** (kotak lebih lebar) dan
sisanya **portrait** (kotak lebih tinggi) — jadi usahakan taruh foto dengan
orientasi yang kurang lebih sesuai supaya nggak terlalu ke-crop. Kalau mau
lihat/ubah foto mana yang portrait/landscape atau ubah kemiringannya, cari
`const galleryData` di bagian bawah `index.html` — tiap baris isinya
`{ rot: <derajat miring>, o: 'p' }` (p = portrait) atau `o: 'l'` (landscape).

> Tips: kalau foto kamu format `.png` atau `.jpeg`, tinggal ganti nama filenya
> jadi `photo1.jpg` dst (rename aja, nggak perlu convert beneran — browser
> tetap bisa baca) atau edit bagian `src="assets/img/photo1.jpg"` di index.html.

## 4. Ubah teks
- Nama & sapaan ada di beberapa tempat di `index.html` — cari kata "Inesa" untuk edit.
- Isi surat ada di bagian `const letterParagraphs = [...]` di bagian bawah file,
  gampang dicari dan diedit.
- Caption di antara foto ("Masih inget ini nggak?", dll) ada di `<p class="gallery-caption">`.
- Jumlah klik tiup lilin (default 12) ada di `const TOTAL_BLOWS = 12;`.

## 5. Cara buka / kirim ke Inesa
- Buka `index.html` langsung di browser HP/laptop untuk cek dulu.
- Untuk dikirim ke Inesa, paling gampang upload seluruh folder
  `birthday-surprise/` ke hosting gratis seperti **Netlify Drop**
  (netlify.com/drop, tinggal drag-drop foldernya) atau **Vercel**, lalu kirim
  link-nya. Bisa juga pakai GitHub Pages kalau familiar.

Selamat mengejutkan Inesa! 🤎🎂
