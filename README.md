
# 🕹️ Neon Tetris Mobile Pro
Aplikasi game Tetris berbasis web yang dioptimalkan khusus untuk perangkat seluler (*mobile-first*). Game ini mengusung estetika **Neon/Cyberpunk** dengan kontrol sentuh yang responsif dan efek suara retro.
## ✨ Fitur Unggulan
 * **Responsive Engine**: Layar game otomatis menyesuaikan ukuran (scaling) berdasarkan dimensi layar HP pengguna.
 * **Virtual Controller**: Tombol kontrol besar yang nyaman digunakan dengan jempol.
 * **Retro Sound Effects**: Menggunakan *Web Audio API* untuk menghasilkan suara *synth* tanpa perlu file audio eksternal.
 * **Haptic Feedback**: Getaran halus (vibrasi) saat berhasil menghancurkan baris (khusus Android).
 * **Next Piece Preview**: Panel kecil untuk melihat balok berikutnya agar pemain bisa menyusun strategi.
## 🚀 Cara Menjalankan
Karena proyek ini hanya terdiri dari satu file HTML, kamu bisa menjalankannya dengan sangat mudah:
 1. Simpan kode ke dalam file bernama index.html.
 2. Buka file tersebut di browser (Chrome/Safari direkomendasikan).
 3. **Untuk pengalaman terbaik di HP**:
   * Gunakan fitur "Add to Home Screen" pada browser HP agar aplikasi berjalan seperti aplikasi native (tanpa bar alamat).
## 🛠️ Detail Teknis
### Arsitektur Kode
 * **Canvas API**: Digunakan untuk merender grid game dan animasi balok.
 * **Matrix Logic**: Arena game direpresentasikan sebagai array 2D [20][12].
 * **Audio Synthesis**: Suara dibuat secara programatik menggunakan OscillatorNode untuk efisiensi performa.
### Struktur Fungsi Utama
| Fungsi | Deskripsi |
|---|---|
| resize() | Menghitung rasio aspek dan skala canvas agar pas di layar. |
| playSound() | Logika utama penghasil suara *square* dan *triangle wave*. |
| arenaSweep() | Mengecek baris yang penuh, menghapusnya, dan menambah skor. |
| playerReset() | Mengambil balok dari antrean 'Next' dan membuat balok baru. |
## 🎨 Kustomisasi
Kamu bisa mengubah tema warna dengan memodifikasi variabel CSS di bagian :root:
```css
:root {
    --neon-blue: #00f3ff;
    --neon-pink: #ff00ff;
    --bg-color: #050505;
}

```
## 📝 Lisensi
MIT
### Tips dari Partner Coding:
Jika kamu ingin meng-hosting game ini agar bisa dimainkan teman-temanmu, kamu bisa menggunakan layanan gratis seperti **GitHub Pages** atau **Netlify**. Cukup unggah file index.html tersebut, dan game kamu akan langsung online!
Apakah ada bagian lain dari dokumentasi atau fitur tambahan yang ingin kamu masukkan ke dalam README ini?
