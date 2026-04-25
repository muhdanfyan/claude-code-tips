# Claude Code: Panduan Workflow & Tips Lanjutan (Deep Dive)

![Claude Code](https://code.claude.com/assets/hero-terminal.png)

Repository ini adalah panduan komprehensif untuk menguasai **Claude Code**, AI CLI otonom dari Anthropic. Materi di sini dikembangkan berdasarkan wawasan dari Boris Cherny (pencipta Claude Code) untuk mengoptimalkan pengalaman coding Anda.

---

## 🧠 Pemahaman Filosofi: Agentic Workflow
Claude Code bukan sekadar chatbot di terminal; ia adalah sebuah **Agent**. Perbedaan utamanya adalah kemampuannya untuk:
1. **Membaca Konten:** Memahami struktur direktori dan isi file secara mendalam.
2. **Menjalankan Perintah:** Menjalankan `npm test`, `git commit`, atau script custom.
3. **Self-Correct:** Jika sebuah perintah gagal (misal: test error), ia akan menganalisis outputnya dan mencoba memperbaikinya secara otomatis.

---

## 🚀 Perintah "Slash" yang Mengubah Permainan

### 1. `/btw` (By The Way) - Konteks Tanpa Gangguan
Seringkali saat Claude sedang mengerjakan tugas besar (seperti refactoring 10 file), Anda teringat sesuatu.
- **Workflow Lama:** Menunggu selesai atau menghentikan proses.
- **Workflow Baru:** Gunakan `/btw`. Claude akan memberikan jawaban cepat menggunakan konteks saat ini tanpa menghentikan "tugas utama" yang sedang ia kerjakan di latar belakang.
- *Contoh:* `/btw "Ngomong-ngomong, apakah fungsi ini sudah mendukung async?"`

### 2. `/loop` - Otomatisasi Observasi
Mengubah Claude menjadi pengawas (monitor).
- **Workflow:** Jalankan prompt secara berulang dengan interval tertentu.
- **Kasus Penggunaan:** Memantau log produksi, mengecek status build CI/CD, atau menunggu email masuk.
- *Contoh:* `/loop "Cek file error.log setiap 10 menit. Jika ada error 'Timeout', berikan ringkasannya."`

### 3. `/schedule` - Eksekusi Jangka Panjang
Memisahkan tugas dari sesi terminal Anda.
- **Desktop:** Berjalan selama aplikasi Claude terbuka.
- **Cloud:** Berjalan di server Anthropic. Sangat cocok untuk tugas yang memakan waktu lama (seperti migrasi database besar atau audit keamanan seluruh repo).

---

## 👁️ Visual Verification: Build-Test-Verify
Integrasi dengan **Chrome Extension** memungkinkan Claude memiliki "mata".
- **Step 1:** Claude menulis kode UI (React/HTML).
- **Step 2:** Claude menjalankan server lokal.
- **Step 3:** Claude membuka browser secara otomatis, mengambil screenshot, dan mendeteksi jika ada elemen yang berantakan atau error di console.
- **Step 4:** Claude memperbaiki kode berdasarkan apa yang ia "lihat".

---

## 📂 Manajemen Ruang Kerja (Workspace)

### Akses Multi-Direktori
Jangan membatasi Claude hanya pada satu folder. Gunakan flag `--add-dir` untuk memberikan referensi library atau dokumentasi eksternal.
```bash
claude --add-dir ../shared-components --add-dir ../api-docs
```

---

## 📱 Mobile & Remote Control: Dispatch
Fitur **Dispatch** memungkinkan Anda mengontrol sesi Claude di PC melalui smartphone. 
- Anda bisa sedang berada di luar rumah, namun memerintahkan Claude di PC kantor untuk menjalankan build atau mengirimkan laporan via Slack melalui aplikasi mobile.

---
*Referensi: [XDA Developers - Claude Code Creator Tips](https://www.xda-developers.com/claude-codes-creator-keeps-sharing-tips-and-they-all-made-my-experience-better/)*
