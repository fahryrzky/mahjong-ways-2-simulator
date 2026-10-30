# Mahjong Ways 2 - Simulator Edukasi Pembongkar Manipulasi Mesin Slot

Proyek simulasi interaktif untuk mendemonstrasikan secara nyata bagaimana algoritma mesin slot (Mahjong Ways 2 oleh PG Soft) memanipulasi psikologi pemain (Near-Miss, Loss Disguised as Win, dan House Edge).

## Arsitektur Aplikasi
1. **Layar Pemain (`/` atau `index.html`)**:
   - Tampilan visual murni 100% seperti game *Mahjong Ways 2* asli (2.000 Ways, ubin emas jadi Wild, pengali x1 s/d x5 atau x2 s/d x10 di Free Spins).
   - **TIDAK ADA notifikasi atau tulisan edukasi** sama sekali di layar pemain, sehingga pemain (ayah) mengira sedang bermain game biasa tanpa curiga.
2. **Layar Backend / Admin (`/admin` atau `admin.html`)**:
   - Dibuka di HP atau laptop anak.
   - Terhubung secara real-time via WebRTC (PeerJS).
   - Menampilkan radar kerugian riil, saldo terkini, dan tombol kendali nasib putaran saat pemain memencet tombol PUTAR.

## Cara Menggunakan:
1. Buka halaman `/admin` di HP/laptop Anda.
2. Salin link game pemain (`/?room=bapa`) lalu buka di HP ayah Anda.
3. Saat ayah memencet tombol PUTAR di HP-nya, layar admin Anda akan berkedip memberi pilihan hasil putaran:
   - **KALAH (ZONK)**
   - **MENANG PALSU (LDW)**
   - **NEAR MISS (HAMPIR KENA)**
   - **PANCINGAN MENANG (HOOK)**
   - **FREE SPINS (3 SCATTER)**
4. Anda bisa melihat reaksi ayah dan langsung menjelaskan manipulasi yang baru saja terjadi.
