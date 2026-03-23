# ZeroXyap - X/Twitter AI Auto-Reply Extension

ZeroXyap adalah ekstensi Google Chrome yang memungkinkan Anda menghasilkan balasan otomatis (*auto-reply*) secara instan dan realistis di X.com (Twitter) [file:5]. Ekstensi ini ditenagai oleh **Mistral AI** untuk menyusun balasan yang natural, interaktif, dan seperti manusia sungguhan [file:3].

## ✨ Fitur Utama
- **Balasan Otomatis Berbasis AI**: Membaca konteks tweet secara otomatis (termasuk *Quote Retweets* dan cuitan biasa) untuk menghasilkan balasan yang relevan menggunakan Mistral AI [file:3][file:7].
- **Dukungan Multi-Model**: Selain Mistral AI, ekstensi ini secara internal memiliki konfigurasi untuk mendukung Google Gemini, Ollama (untuk AI lokal), dan layanan Novita AI [file:3][file:5].
- **Pilihan Persona/Tone**: Dilengkapi dengan UI pop-up di layar untuk memilih "tone" atau gaya bahasa agar balasan sesuai dengan preferensi Anda [file:7].
- **Keamanan & Lisensi**: Terintegrasi langsung dengan Supabase untuk otentikasi kunci lisensi (*license key*) pengguna dan manajemen sesi yang aman [file:3].
- **Integrasi Seamless di X.com**: Tombol AI disuntikkan langsung ke dalam antarmuka X.com, mendukung baik *Dark Mode* (mode gelap) maupun *Light Mode* [file:7].

## 🛠️ Persyaratan Sistem
- Google Chrome atau browser berbasis Chromium lainnya (Edge, Brave, dll).
- Kunci Lisensi (License Key) yang aktif untuk melewati layar otentikasi [file:3].

## 🚀 Cara Instalasi (Local / Developer Mode)
1. Unduh atau *clone* repositori ini ke komputer Anda.
2. Jika berformat zip, ekstrak folder tersebut.
3. Buka browser Chrome dan navigasikan ke halaman ekstensi: `chrome://extensions/`.
4. Aktifkan sakelar **Developer mode** di sudut kanan atas layar.
5. Klik tombol **Load unpacked** dan pilih folder tempat Anda menyimpan file ekstensi ini (folder yang berisi `manifest.json`) [file:5].
6. Ekstensi ZeroXyap akan muncul di daftar ekstensi Anda.

## 💡 Cara Penggunaan
1. Klik ikon ekstensi ZeroXyap di *toolbar* browser Anda. Anda akan diarahkan ke halaman `login.html` untuk memverifikasi Kunci Lisensi Anda [file:3][file:5].
2. Buka [X.com](https://x.com) dan masuk ke akun Anda.
3. Saat Anda membuka sebuah cuitan atau ingin membalas (*reply*), Anda akan melihat tombol baru bertenaga AI di dekat kolom teks [file:7].
4. Klik tombol tersebut, pilih "tone/persona" yang diinginkan, dan ekstensi akan mengambil teks target untuk diproses oleh Mistral AI [file:3][file:7].
5. Tinjau hasil balasan yang dimasukkan ke kotak teks, lalu klik "Reply" di Twitter seperti biasa.

## 📂 Struktur Repositori
- `manifest.json`: Berisi definisi ekstensi berbasis Manifest V3 [file:5].
- `background.js`: Service worker yang menangani pemanggilan API ke AI (Mistral, Gemini, Ollama) dan validasi database Supabase [file:3].
- `content.js`: Script yang mendeteksi tweet di antarmuka X.com dan menampilkan komponen UI seperti tombol AI dan menu *Tone Selector* [file:7].
- `popup.html` & `login.html`: Tampilan layar ekstensi utama dan layar otentikasi pengguna [file:4][file:1].
