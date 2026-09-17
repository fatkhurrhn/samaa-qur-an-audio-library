# ![Samaa Banner](https://img.shields.io/badge/Samaa-Qur'an%20Audio%20Library-10b981?style=for-the-badge)

> A modern, full-featured web application for managing and streaming Qur'an audio recitations from Cloudflare R2 storage, with Firebase as metadata backend.


![React](https://img.shields.io/badge/React-18-61dafb?style=flat-square&logo=react)
![Firebase](https://img.shields.io/badge/Firebase-Firestore-ffca28?style=flat-square&logo=firebase)
![Cloudflare R2](https://img.shields.io/badge/Cloudflare-R2-f38020?style=flat-square&logo=cloudflare)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38bdf8?style=flat-square&logo=tailwindcss)

---

## Tentang Project

**Samaa** (سَمَاعٌ — "mendengar") adalah platform manajemen & streaming audio Qur'an yang dirancang untuk mengelola koleksi murottal dari banyak qari/syeikh secara efisien. Aplikasi ini menggabungkan **Cloudflare R2** sebagai object storage untuk file audio dan **Firebase Firestore** sebagai backend metadata.

Dibangun dengan fokus pada:
- **Pengalaman mendengarkan yang nyaman** — floating audio player dengan kontrol lengkap
- **Sinkronisasi cepat** — batch write ke Firestore hingga 400 dokumen per commit
- **UI modern & responsif** — bekerja optimal di desktop maupun mobile
- **Realtime update** — data syeikh tersinkron otomatis via Firestore `onSnapshot`

---

## Fitur Utama

### Manajemen Audio
- **Auto-discovery** — file audio di R2 otomatis ter-scan dan dikelompokkan per syeikh
- **Sinkronisasi selektif** — sync satu surah, per syeikh, atau seluruh koleksi sekaligus
- **Batch processing** — sinkronisasi ribuan file dengan chunking otomatis (max 400/batch)
- **Skip existing** — file yang sudah tersync otomatis dilewati, hanya proses yang baru
- **Delete sync** — hapus entri dari Firebase tanpa menyentuh file di R2

### Metadata Syeikh
- Profil lengkap: nama, asal, tanggal lahir, deskripsi, foto
- Realtime update lintas tab/device
- Preview foto langsung di sidebar

### Floating Audio Player
- Kontrol lengkap: play/pause, next/prev, seek, mute
- Auto-play surah berikutnya
- Progress bar interaktif
- Expand/collapse mode
- Persistent di semua halaman

### Dashboard & Analytics
- Statistik global: total file, syeikh, surah unik, total ukuran
- Progress sync per syeikh & global
- Ranking syeikh berdasarkan jumlah koleksi

### Pencarian Cerdas
- Cari syeikh berdasarkan nama atau slug
- Cari surah berdasarkan nomor, nama Arab, nama Latin, atau arti

