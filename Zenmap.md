# Zenmap

Zenmap adalah antarmuka grafis untuk Nmap, yang merupakan salah satu alat pemindaian jaringan paling populer dan kuat yang digunakan untuk berbagai tujuan keamanan dan administrasi jaringan.

Zenmap membuat penggunaan Nmap lebih mudah dengan menyediakan antarmuka grafis yang intuitif untuk konfigurasi dan interpretasi hasil pemindaian.

Fitur Utama Zenmap

  + Antarmuka Grafis Pengguna (GUI)
        Zenmap menyediakan antarmuka grafis yang memudahkan pengguna untuk mengonfigurasi dan menjalankan pemindaian Nmap tanpa harus menggunakan baris perintah.

  + Profil Pemindaian
        Menyediakan berbagai profil pemindaian bawaan dan memungkinkan pengguna untuk membuat dan menyimpan profil pemindaian kustom untuk digunakan kembali.

  + Visualisasi Hasil
        Menampilkan hasil pemindaian dalam format yang mudah dibaca, termasuk tabel, grafik, dan peta topologi jaringan (jika diaktifkan).

  + Pemetaan Jaringan
        Menyediakan kemampuan untuk menghasilkan peta topologi jaringan dari hasil pemindaian, membantu dalam visualisasi struktur jaringan.

  + Ekspor dan Laporan
        Memungkinkan ekspor hasil pemindaian ke berbagai format seperti XML, grepable, atau file teks untuk analisis lebih lanjut atau dokumentasi.

  + Integrasi dengan Nmap
        Zenmap sepenuhnya terintegrasi dengan Nmap, memanfaatkan semua fitur dan kemampuan pemindaian Nmap sambil menyederhanakan antarmuka pengguna.

gambar 1 Tampilan awal zenmap

![image](https://github.com/user-attachments/assets/51dbb40c-c108-42ca-9153-29c91d599dce)

Contoh Penggunaan Zenmap

  scan Dasar:
        
 `Untuk melakukan pemindaian dasar, masukkan IP atau domain target dan pilih profil seperti "Intense Scan" dari menu dropdown. Klik "Scan" untuk memulai.`

  Scan Kustom:
  
  `Untuk konfigurasi lebih lanjut, masukkan opsi Nmap secara manual di kolom "Command". Misalnya:`


    -sS -p 22,80,443 --open -T4

Ini akan melakukan pemindaian SYN stealth, memeriksa port 22, 80, dan 443, hanya menampilkan port yang terbuka, dan menggunakan waktu pemindaian yang lebih cepat.

