# Bongkar Calculator Pro

Versi GitHub Pages Open Here.

## Fitur
- Riwayat transaksi dan perhitungan HD/LC.
- Pengaturan harga, saldo, template ID/pesan, bahasa, dan tema.
- Penyimpanan lokal di browser (`localStorage`).
- Backup dan pemulihan data melalui JSON.

## Penting: cara kerja data
- Website bisa diakses online, tetapi data transaksi dan pengaturan disimpan di browser/perangkat yang sedang digunakan. Data tidak dikirim ke GitHub dan tidak otomatis sinkron antarperangkat.
- Sebelum membersihkan data browser, mengganti browser, atau pindah perangkat, klik tombol backup (ikon database) dan simpan file JSON di tempat aman.
- Di perangkat lain, buka aplikasi lalu gunakan tombol restore (ikon upload) dan pilih file backup JSON.
- Jangan memasukkan data sensitif jika perangkat dipakai bersama orang lain.

## Mode offline
Service worker menyimpan halaman aplikasi dan mencoba menyimpan aset CDN saat aset tersebut diminta ketika online. Buka aplikasi sekali dengan internet terlebih dahulu. Namun Tailwind, font Google, dan Lucide masih berasal dari CDN; mode offline penuh tidak bisa dijamin jika aset belum tersimpan atau CDN berubah/tidak tersedia. Untuk penggunaan offline yang benar-benar mandiri, aset-aset tersebut sebaiknya dibundel langsung di repository.

## Catatan
`localStorage` terikat pada origin dan browser. Mengganti URL/domain, browser, atau perangkat bisa membuat data tampak kosong; gunakan backup JSON secara berkala.
