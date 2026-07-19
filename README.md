# FileDetect (.asi)

Plugin anticheat sisi client untuk SA-MP. Mendeteksi module, proses, dan file yang umum dipakai untuk cheat/mod di GTA:SA, lalu melaporkannya ke admin server lewat webhook Discord.

Client-side anticheat plugin for SA-MP. Detects modules, processes, and files commonly used for cheating/modding in GTA:SA, then reports them to the server admin via a Discord webhook.

## Cara Kerja / How It Works

**Bahasa Indonesia**

Setelah masuk ke server, plugin ini akan memeriksa:

- Module yang ter-load di dalam game (`.asi`, `.dll`)
- Proses lain yang sedang berjalan di komputer (Cheat Engine, injector, debugger, dll)
- File dan folder di direktori game (folder `CLEO`, `moonloader`, `SAMPFUNCS`/`sampfun`, file `.asi` di root, serta script `.cs` / `.lua` / `.luac` / `.sf`)

Kalau ada temuan, laporan dikirim ke server yang sedang kamu mainkan. Laporan berisi:

- Username pemain di server SA-MP
- Alamat IP dan port server
- Nama komputer dan username Windows kamu
- Daftar temuan, dikelompokkan jadi: ASI, Lua/MoonLoader, CLEO, SAMPFUN, dan Lainnya

Kalau tidak ada temuan sama sekali, tidak ada apa pun yang dikirim.

**English**

After joining a server, this plugin checks:

- Modules loaded inside the game (`.asi`, `.dll`)
- Other processes running on your computer (Cheat Engine, injectors, debuggers, etc.)
- Files and folders in the game directory (`CLEO`, `moonloader`, `SAMPFUNCS`/`sampfun` folders, `.asi` files in the root, and `.cs` / `.lua` / `.luac` / `.sf` scripts)

If anything is found, a report is sent to the server you are currently playing on. The report includes:

- The player's SA-MP username
- The server's IP address and port
- Your computer name and Windows username
- The list of findings, grouped into: ASI, Lua/MoonLoader, CLEO, SAMPFUN, and Other

If nothing is found, nothing is sent at all.

## Instalasi / Installation

**Bahasa Indonesia**

1. Salin file `.asi` plugin ini ke folder utama GTA:SA (folder yang sama dengan `gta_sa.exe` / `samp.exe`).
2. Jalankan game dan connect ke server seperti biasa.

**English**

1. Copy this plugin's `.asi` file into your main GTA:SA folder (the same folder as `gta_sa.exe` / `samp.exe`).
2. Launch the game and connect to a server as usual.

## Yang Perlu Diketahui / What You Should Know

**Bahasa Indonesia**

- Plugin ini hanya berjalan untuk mendeteksi, bukan untuk memblokir atau menutup game kamu secara otomatis. Tindakan (kick/ban) sepenuhnya keputusan admin server berdasarkan laporan yang masuk.
- Semua file `.asi` yang bukan bagian dari core game akan dilaporkan sebagai "ASI tidak dikenal", termasuk mod visual/QoL yang mungkin kamu anggap tidak berbahaya. Ini disengaja: keputusan mod mana yang diizinkan ada di tangan admin server, bukan plugin ini.
- Laporan hanya terkirim ke server yang IP dan port-nya sudah terdaftar di sistem pemilik plugin ini. Kalau server belum terdaftar, laporan otomatis tidak terkirim ke mana pun.

**English**

- This plugin only detects; it does not block or close your game automatically. Any action (kick/ban) is entirely up to the server admin, based on the reports received.
- Every `.asi` file that is not part of the core game will be reported as "unknown ASI," including visual/QoL mods you might consider harmless. This is intentional: deciding which mods are allowed is up to the server admin, not this plugin.
- Reports are only sent for servers whose IP and port are already registered in this plugin's system. If a server is not registered, no report is sent anywhere.

## Kekurangan / Limitations

**Bahasa Indonesia**

- Karena berbentuk file `.asi`, plugin ini mewajibkan setiap player untuk mengunduh dan memasang file tersebut secara manual di folder game. Player yang tidak memasangnya berarti tidak terpantau oleh sistem ini sama sekali.
- File `.asi` hanya berjalan sebagai module Windows (PE/DLL yang di-load oleh ASI loader), sehingga tidak bisa dipakai di GTA:SA versi Android/mobile. Player yang bermain lewat HP tidak akan terdeteksi oleh plugin ini, apa pun kondisi perangkat mereka.
- Karena bergantung pada instalasi manual, cara ini tidak bisa memaksa (enforce) semua player memakainya — sifatnya opsional/himbauan, bukan wajib di level server.

**English**

- Because it ships as an `.asi` file, this plugin requires every player to manually download and install it in their game folder. Players who don't install it are not monitored by this system at all.
- The `.asi` file only runs as a Windows module (a PE/DLL loaded by an ASI loader), so it cannot be used on the Android/mobile version of GTA:SA. Players on mobile will never be detected by this plugin, regardless of what's on their device.
- Since it relies on manual installation, this approach cannot be enforced on every player — it's optional/recommended, not mandatory at the server level.

## Pendaftaran Server / Server Registration (untuk Admin/Owner Server)

**Bahasa Indonesia**

Server harus terdaftar terlebih dahulu supaya laporan dari plugin ini bisa diteruskan ke webhook Discord server kamu. Pendaftaran dilakukan melalui:

**English**

Your server must be registered first so reports from this plugin can be forwarded to your Discord webhook. Registration is done at:

https://samp.derrick.web.id/
