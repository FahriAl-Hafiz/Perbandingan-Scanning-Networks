# Nmap

Nmap (Network Mapper) adalah tool open-source yang digunakan untuk melakukan pemindaian dan analisis jaringan. Ini adalah salah satu alat paling populer di bidang keamanan jaringan dan digunakan oleh administrator jaringan serta para profesional keamanan untuk memetakan jaringan, mengidentifikasi perangkat yang terhubung, dan mengevaluasi status keamanan.

Berikut adalah fungsi utama Nmap:

  + Pemindaian Port: Nmap memeriksa port pada perangkat yang terhubung ke jaringan untuk melihat port mana yang terbuka dan layanan apa yang berjalan di atasnya.

  + Deteksi Layanan (Service Detection): Nmap dapat mengidentifikasi aplikasi atau layanan yang berjalan pada port tertentu, seperti HTTP, FTP, SSH, dan lainnya.

  + Mendeteksi Sistem Operasi (OS Detection): Nmap mampu memperkirakan sistem operasi yang digunakan oleh perangkat berdasarkan perilaku jaringan mereka.

  + Penemuan Host (Host Discovery): Nmap digunakan untuk mengetahui perangkat apa saja yang terhubung ke jaringan, bahkan yang mungkin tidak aktif merespons ping.

  + Audit Keamanan: Administrator jaringan menggunakannya untuk menemukan kelemahan atau celah keamanan dalam jaringan, seperti port yang tidak seharusnya terbuka atau layanan yang tidak aman.

  + Pemetaan Jaringan (Network Mapping): Nmap memungkinkan pengguna untuk memahami topologi jaringan, seperti struktur perangkat yang terhubung dan bagaimana mereka saling berinteraksi.

nmap memiliki beberapa perintah atau opsi (flags) yang umum digunakan untuk pemindaian jaringan. Berikut adalah beberapa perintah (atau opsi) yang dapat digunakan bersama nmap:

-sS: SYN scan, salah satu metode scanning tercepat yang digunakan untuk mendeteksi port terbuka.

bash

    nmap -sS <target>

-sP: Ping scan, hanya untuk memeriksa apakah host hidup (aktif atau tidak).

bash

    nmap -sP <target>

-O: Mendeteksi sistem operasi target.

bash

    nmap -O <target>

-sV: Menemukan versi layanan yang berjalan di port terbuka.

bash

    nmap -sV <target>

-p: Menentukan port spesifik yang akan dipindai.

bash

    nmap -p 80,443 <target>

-A: Melakukan pemindaian agresif (mendeteksi OS, versi layanan, script, dan traceroute).

bash

    nmap -A <target>

-T4: Mempercepat proses scanning (T0-T5 adalah opsi kecepatan, T5 paling cepat).

bash

nmap -T4 <target>

    -Pn: Memindai tanpa ping (biasanya digunakan untuk host yang menolak ICMP ping).

bash

    nmap -Pn <target>
