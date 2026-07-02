# Client-AC (.asi)

Plugin anticheat sisi client untuk SA-MP. Mendeteksi module, proses, dan file yang umum dipakai untuk cheat/mod di GTA:SA, lalu melaporkannya ke admin server lewat webhook Discord.

## Cara Kerja

Setelah masuk ke server, plugin ini akan memeriksa:

- Module yang ter-load di dalam game (`.asi`, `.dll`)
- Proses lain yang sedang berjalan di komputer (Cheat Engine, injector, debugger, dll)
- File dan folder di direktori game (folder `CLEO`, `moonloader`, `SAMPFUNCS`/`sampfun`, file `.asi` di root, serta script `.cs` / `.lua` / `.luac` / `.sf`)

Kalau ada temuan, laporan dikirim ke server yang sedang kamu mainkan. Laporan berisi:

- Alamat IP dan port server
- Nama komputer dan username Windows kamu
- Daftar temuan, dikelompokkan jadi: ASI, Lua/MoonLoader, CLEO, SAMPFUN, dan Lainnya

Kalau tidak ada temuan sama sekali, tidak ada apa pun yang dikirim.

## Instalasi

1. Salin file `.asi` plugin ini ke folder utama GTA:SA (folder yang sama dengan `gta_sa.exe` / `samp.exe`).
2. Jalankan game dan connect ke server seperti biasa.

## Yang Perlu Diketahui

- Plugin ini hanya berjalan untuk mendeteksi, bukan untuk memblokir atau menutup game kamu secara otomatis. Tindakan (kick/ban) sepenuhnya keputusan admin server berdasarkan laporan yang masuk.
- Semua file `.asi` yang bukan bagian dari core game akan dilaporkan sebagai "ASI tidak dikenal", termasuk mod visual/QoL yang mungkin kamu anggap tidak berbahaya. Ini disengaja: keputusan mod mana yang diizinkan ada di tangan admin server, bukan plugin ini.
- Laporan hanya terkirim ke server yang IP dan port-nya sudah terdaftar di sistem pemilik plugin ini. Kalau server belum terdaftar, laporan otomatis tidak terkirim ke mana pun.

## Pendaftaran Server (untuk Admin/Owner Server)

Server harus terdaftar terlebih dahulu supaya laporan dari plugin ini bisa diteruskan ke webhook Discord server kamu. Pendaftaran dilakukan melalui:

https://samp-api-blue.vercel.app/
