☀️ Aplikasi Cuaca Interaktif
Aplikasi Cuaca Interaktif adalah proyek front-end sederhana yang memungkinkan pengguna untuk mencari dan melihat 
informasi cuaca terkini serta prakiraan cuaca per jam dan per hari untuk berbagai kota di seluruh dunia. Aplikasi ini 
dibangun dengan fokus pada antarmuka pengguna yang bersih dan responsif menggunakan Tailwind CSS.

✨ Fitur Utama
Pencarian Kota: Cari informasi cuaca untuk kota mana pun dengan mudah.
Cuaca Terkini: Menampilkan suhu, kondisi cuaca, dan ikon yang relevan secara real-time.
Prakiraan Per Jam: Lihat perkiraan cuaca mendetail untuk beberapa jam ke depan.
Prakiraan Per Hari: Dapatkan ringkasan cuaca harian untuk beberapa hari ke depan (suhu min/maks, kondisi).
Riwayat Pencarian: Menyimpan 5 pencarian kota terakhir untuk akses cepat.
Responsif: Desain yang menyesuaikan untuk berbagai ukuran layar (desktop dan mobile).

💻 Teknologi yang Digunakan

* HTML5: Untuk struktur dasar halaman web.
* CSS3 (dengan Tailwind CSS): Untuk styling dan *layout* yang modern dan responsif. Tailwind CSS mempercepat pengembangan antarmuka dengan utility classes yang fleksibel.
* JavaScript (Vanilla JS): Untuk logika aplikasi, *fetching* data dari API, dan manipulasi DOM.
* OpenWeatherMap API: Digunakan untuk mendapatkan data cuaca terkini dan prakiraan.

🚀 Cara Menjalankan Aplikasi

Aplikasi ini adalah proyek *front-end* murni, jadi kamu tidak memerlukan *server* *back-end* untuk menjalankannya.

1.  Kloning Repositori (jika ada):
    ```bash
    git clone [URL_REPOSITORI_ANDA]
    cd [nama-folder-aplikasi]
    ```
    Jika tidak ada repositori, cukup simpan kode HTML ke dalam file `.html` (misalnya `index.html`).

2.  Buka di Peramban:
    Buka file `index.html` (atau nama file HTML yang kamu gunakan) langsung di peramban web pilihan kamu (misalnya Google Chrome, Mozilla Firefox). Kamu bisa melakukan ini dengan:
    * Klik dua kali file `index.html`.
    * Klik kanan file `index.html` dan pilih "Open with..." lalu pilih peramban kamu.

3.  Kunci API (Penting!):
    Aplikasi ini memerlukan OpenWeatherMap API Key untuk mengambil data cuaca.
    * Daftar untuk mendapatkan API Key gratis di [OpenWeatherMap](https://openweathermap.org/api).
    * Setelah mendapatkan API Key, ganti `YOUR_API_KEY_HERE` (atau `0d52f4451e38bbaf9f1844d2a813e215` jika kamu ingin langsung mencoba dengan API Key
      yang ada di kode) di baris berikut dalam skrip JavaScript:

      javascript
        const app = new WeatherApp('YOUR_API_KEY_HERE');
        
    * Jika kamu menggunakan API Key yang sudah ada di kode, pastikan itu masih aktif dan tidak melebihi batas penggunaan gratis. Sangat disarankan untuk mengganti dengan API Key pribadi kamu.

🛠️ Pengembangan

Kode JavaScript diorganisir dalam sebuah *Class* `WeatherApp` untuk mengelola state dan fungsionalitas aplikasi.

* `constructor(apiKey)`: Menginisialisasi aplikasi dengan API Key dan memuat riwayat dari `localStorage`.
* `setActiveTab(tabName)`: Mengelola pergantian antara tampilan prakiraan "Per jam" dan "Per hari".
* `WorkspaceWeather(city)`: Mengambil data cuaca terkini dan prakiraan dari OpenWeatherMap API.
* `renderCurrentWeather(data)`: Memperbarui tampilan cuaca terkini di UI.
* `renderDailyForecast(forecastData)`: Menampilkan prakiraan cuaca harian.
* `renderHourlyForecast(forecastData)`: Menampilkan prakiraan cuaca per jam.
* `getWeatherEmoji(iconCode)`: Mengkonversi kode ikon cuaca dari API menjadi emoji yang relevan.
* `saveHistory(city)`: Menyimpan kota yang dicari ke `localStorage`.
* `renderHistory()`: Memperbarui daftar riwayat pencarian di UI.

📝 Catatan

* Aplikasi ini menggunakan `localStorage` untuk menyimpan riwayat pencarian. Data akan tetap ada meskipun peramban ditutup, hingga pengguna menghapus cache perambannya.
* Prakiraan per jam menampilkan sekitar 8 jam ke depan, sedangkan prakiraan per hari menampilkan 5 hari ke depan.
* Ikon cuaca direpresentasikan menggunakan emoji untuk kesederhanaan dan kemudahan implementasi.

 🤝 Kontribusi

Jika kamu menemukan bug atau memiliki saran untuk perbaikan, jangan ragu untuk membuka issue atau mengirimkan pull request (jika ini adalah repositori GitHub).

Terima kasih telah melihat proyek Aplikasi Cuaca Interaktif ini
