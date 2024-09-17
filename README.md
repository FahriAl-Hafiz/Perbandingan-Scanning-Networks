# Perbandingan-Scanning-Networks
[Nmap](Nmap.md) | [Zenmap](Zenmap.md) | [Angry Ip Scanner](IpAngryScanner.md) 

**Scanning networks** adalah proses mencari dan mengidentifikasi perangkat, layanan, dan port yang terbuka di dalam jaringan. 

Tujuannya adalah untuk mengumpulkan informasi tentang apa yang berjalan di jaringan tersebut. Biasanya, ini dilakukan oleh administrator untuk menjaga keamanan jaringan, tapi bisa juga digunakan oleh penyerang untuk mencari celah yang bisa dieksploitasi.

Dalam dunia keamanan jaringan dan administrasi sistem, pemindaian jaringan adalah langkah penting untuk mengidentifikasi perangkat, layanan, serta potensi kerentanan dalam jaringan.

Tiga alat yang sering digunakan untuk tugas ini adalah **Nmap, Zenmap, dan Angry IP Scanner**. Meskipun ketiganya memiliki fungsi utama yang sama, yaitu memindai dan memetakan jaringan, masing-masing memiliki keunikan dalam hal antarmuka, fitur, dan penggunaannya.

## 1. Nmap :

Nmap adalah salah satu alat pemindaian jaringan yang paling kuat dan banyak digunakan dalam keamanan siber. Alat ini dirancang untuk memindai jaringan dan mengidentifikasi host, port terbuka, serta layanan yang berjalan pada jaringan tersebut. Fungsi utamanya meliputi pemindaian port, deteksi sistem operasi (OS detection), dan pencarian layanan yang tersedia di host tertentu. Karena sifatnya yang sangat fleksibel, Nmap mendukung berbagai teknik pemindaian, termasuk pemindaian TCP, UDP, SYN, FIN, dan lain-lain.

Keunggulan Nmap terletak pada kemampuannya yang mendalam dan detail dalam melakukan pemetaan jaringan, serta kemampuannya untuk dikustomisasi dengan berbagai opsi dan skrip (seperti Nmap Scripting Engine, NSE). Namun, Nmap lebih berorientasi pada pengguna yang nyaman dengan antarmuka baris perintah (CLI), sehingga bisa jadi agak rumit untuk pengguna baru yang tidak terbiasa dengan command-line.
## 2. Zenmap :

Zenmap adalah versi antarmuka grafis (GUI) dari Nmap. Alat ini dirancang untuk pengguna yang kurang nyaman dengan antarmuka baris perintah dan ingin pengalaman yang lebih visual dan intuitif dalam menggunakan Nmap. Meskipun Zenmap menggunakan mesin pemindaian Nmap di latar belakang, antarmuka grafisnya memudahkan pengguna dalam menavigasi dan melakukan pemindaian dengan klik dan pengaturan yang lebih mudah dimengerti.

Zenmap memungkinkan pengguna untuk menyimpan hasil pemindaian dan membandingkannya dari waktu ke waktu, sehingga sangat cocok untuk tugas pemantauan jaringan berulang. Meskipun memiliki fitur yang sama dengan Nmap, Zenmap membuat penggunaan alat ini lebih ramah bagi pemula yang membutuhkan akses cepat tanpa harus mengingat sintaks baris perintah yang rumit.
## 3. Angry IP Scanner :

Angry IP Scanner adalah alat pemindaian jaringan yang terkenal karena kesederhanaan dan kecepatannya. Tidak seperti Nmap yang lebih detail dan mendalam, Angry IP Scanner lebih fokus pada pemindaian IP dan port secara cepat di jaringan lokal maupun luas. Ini merupakan pilihan populer bagi pengguna yang membutuhkan hasil pemindaian cepat tanpa terlalu banyak detail atau konfigurasi yang rumit.

Angry IP Scanner menyediakan antarmuka pengguna grafis yang sangat sederhana, dan hasil pemindaian ditampilkan secara langsung dalam tabel yang mudah dibaca. Alat ini cocok untuk pengguna yang hanya perlu melakukan pemindaian sederhana dan cepat, seperti mencari perangkat yang aktif di jaringan atau memeriksa port yang terbuka. Meskipun lebih cepat dan mudah digunakan, Angry IP Scanner tidak memiliki kedalaman fitur seperti Nmap dalam hal pemindaian mendalam atau kemampuan skrip.
Perbandingan Utama:

  + Nmap unggul dalam fleksibilitas, kedalaman pemindaian, dan kemampuan scripting, menjadikannya alat yang sangat kuat untuk pengguna yang berpengalaman dalam keamanan jaringan.
  
  + Zenmap menawarkan kemudahan penggunaan dengan antarmuka grafis yang mempermudah akses ke fitur Nmap tanpa mengorbankan fungsionalitasnya, cocok untuk pengguna yang membutuhkan GUI.
  
  + Angry IP Scanner adalah pilihan terbaik untuk pemindaian cepat dan sederhana, ideal bagi pengguna yang membutuhkan informasi dasar seperti perangkat yang aktif di jaringan tanpa banyak konfigurasi atau fitur tambahan.

## Hasil perbandingan dari penggunaan ketiga tools tersebut : 

1.     sudo nmap -sS -A -sV www.dpr.go.id >> nmap.log
   
        cat nmap.log
        Starting Nmap 7.95 ( https://nmap.org ) at 2024-09-17 09:20 EDT
        Nmap scan report for www.dpr.go.id (223.255.230.144)
        Host is up (0.012s latency).
        Other addresses for www.dpr.go.id (not scanned): 223.255.230.168 2600:1417:5c00:20::17d6:a9e1 2600:1417:5c00:20::17d6:a9d3
        rDNS record for 223.255.230.144: subs14-223-255-230-144.three.co.id
        Not shown: 998 filtered tcp ports (no-response)
        PORT    STATE SERVICE VERSION
        80/tcp  open  http    AkamaiGHost (Akamai's HTTP Acceleration/Mirror service)
        |_http-title: Dewan Perwakilan Rakyat
        443/tcp open  ssl
        |_ssl-known-key: ERROR: Script execution failed (use -d to debug)
        | tls-nextprotoneg: 
        |   http/1.1
        |_  http/1.0
        |_ssl-date: TLS randomness does not represent time
        | ssl-cert: OpenSSL required to parse certificate.
        | -----BEGIN CERTIFICATE-----
        | MIIHGzCCBgOgAwIBAgIQC86uXxkIqBcXeYKILRAPQzANBgkqhkiG9w0BAQsFADBP
        | MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMSkwJwYDVQQDEyBE
        | aWdpQ2VydCBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTAeFw0yNDA0MTgwMDAwMDBa
        | Fw0yNTA0MTkyMzU5NTlaMHkxCzAJBgNVBAYTAlVTMRYwFAYDVQQIEw1NYXNzYWNo
        | dXNldHRzMRIwEAYDVQQHEwlDYW1icmlkZ2UxIjAgBgNVBAoTGUFrYW1haSBUZWNo
        | bm9sb2dpZXMsIEluYy4xGjAYBgNVBAMTEWEyNDguZS5ha2FtYWkubmV0MIIBIjAN
        | BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqGpA0e4oRRVGNufJoFuYxBeeqoXQ
        | FXjC/CPHJYG2GMrFoKHFieW9k6I4rNo+C6bOPtX6J361xYJ8Xwi6YfiGyGn15aO/
        | 1bWZw974tVaLJoVjiimVU6XKBVO+GVEs7R8GHlNKOdRh+VLC5ZAiWFcHvEWksBzX
        | mQwgMJT14tXupmSSCef11OTlIHQtDFqU68ZnqEezrs/0ayJUh9yWtWBUCFMIfeX5
        | bvQflOH+s5zAkmYcNxq6NgkKZ+LsvbvJG4pYgVstJZ3rQO6VH7seD6r8JEpc/oWf
        | wREI9gZLPyGH9AnTUflEPeRMYpHbe7e6kEpbRpFTUDMP0Eymp3TQITJyGwIDAQAB
        | o4IDxzCCA8MwHwYDVR0jBBgwFoAUt2ui6qiqhIx56rTaD5iyxZV2ufQwHQYDVR0O
        | BBYEFApfhQi0NX+b0J0gxaF8hxlR7YG0MG4GA1UdEQRnMGWCEWEyNDguZS5ha2Ft
        | YWkubmV0gg8qLmFrYW1haXplZC5uZXSCFyouYWthbWFpemVkLXN0YWdpbmcubmV0
        | gg4qLmFrYW1haWhkLm5ldIIWKi5ha2FtYWloZC1zdGFnaW5nLm5ldDA+BgNVHSAE
        | NzA1MDMGBmeBDAECAjApMCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0
        | LmNvbS9DUFMwDgYDVR0PAQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggr
        | BgEFBQcDAjCBjwYDVR0fBIGHMIGEMECgPqA8hjpodHRwOi8vY3JsMy5kaWdpY2Vy
        | dC5jb20vRGlnaUNlcnRUTFNSU0FTSEEyNTYyMDIwQ0ExLTQuY3JsMECgPqA8hjpo
        | dHRwOi8vY3JsNC5kaWdpY2VydC5jb20vRGlnaUNlcnRUTFNSU0FTSEEyNTYyMDIw
        | Q0ExLTQuY3JsMH8GCCsGAQUFBwEBBHMwcTAkBggrBgEFBQcwAYYYaHR0cDovL29j
        | c3AuZGlnaWNlcnQuY29tMEkGCCsGAQUFBzAChj1odHRwOi8vY2FjZXJ0cy5kaWdp
        | Y2VydC5jb20vRGlnaUNlcnRUTFNSU0FTSEEyNTYyMDIwQ0ExLTEuY3J0MAwGA1Ud
        | EwEB/wQCMAAwggF/BgorBgEEAdZ5AgQCBIIBbwSCAWsBaQB3AM8RVu7VLnyv84db
        | 2Wkum+kacWdKsBfsrAHSW3fOzDsIAAABjvFmI+0AAAQDAEgwRgIhAPVgoJHc/QEU
        | blpkXp9RQq0RofgS0iwnIFMT6J66MTiFAiEAwYvpjkO5d/sVKdKtkQW0HESMen/7
        | shS56B9JU4unWfIAdwB9WR4S4XgqexxhZ3xe/fjQh1wUoE6VnrkDL9kOjC55uAAA
        | AY7xZiO9AAAEAwBIMEYCIQCbHdXugLUCltL848VExmqsH3PpB/92HC0EKNhz1s+5
        | cAIhALCkgautlKPd3OrDgWxP83JgXrhnkA71ppG9yS4y8Hr7AHUA5tIxY0B3jMEQ
        | QQbXcbnOwdJA9paEhvu6hzId/R43jlAAAAGO8WYjygAABAMARjBEAiBz92X8U6tC
        | 6jOPJ8q5K1qXOPZa4IR1eqjfqfuyh4hN/QIgM9mRadEK9GY2rzKuDMwjh7sZNNwz
        | K3ratQbXf9Mu0vcwDQYJKoZIhvcNAQELBQADggEBABGC3vRlpdBmST0RKziaE2ZF
        | 0gZGbmDakDbCKB2eQbmprybedKbjq9Qc5bidncwxYt5hXg06/ZXMpG2QQLVgbPqG
        | J+NOkWJZM3qL83DWAXp4vg29cRK3MDtDXLNRrcWbkqXE6oZDuiCMtGiBIadVjrcH
        | 2lb0jP3k+CESdRBtvnFW5pUumqcCQIEbL062pqemNyllSgbKmmdvgXKuc5QQROIA
        | LM3nmi3p1d50GvNh25EX01A4oGFT7n8ZQRFZHLzKvTKRVnhComy+UDNPLM5iAr0E
        | GJAqBLsUGDmKZg3PSXqkl8z7CygfECpmRZyPOrDSKIPXbfTpu3B5cmFx9U7FxXY=
        |_-----END CERTIFICATE-----
        | tls-alpn: 
        |   http/1.1
        |_  http/1.0
        Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
        Device type: WAP|general purpose
        Running: Actiontec embedded, Linux 2.4.X
        OS CPE: cpe:/h:actiontec:mi424wr-gen3i cpe:/o:linux:linux_kernel cpe:/o:linux:linux_kernel:2.4.37
        OS details: Actiontec MI424WR-GEN3I WAP, DD-WRT v24-sp2 (Linux 2.4.37)
        Network Distance: 2 hops
        
        TRACEROUTE (using port 80/tcp)
        HOP RTT     ADDRESS
        1   0.20 ms 192.168.159.2
        2   0.17 ms subs14-223-255-230-144.three.co.id (223.255.230.144)
        
        OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
        Nmap done: 1 IP address (1 host up) scanned in 71.96 seconds



