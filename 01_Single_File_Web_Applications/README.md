# 01: Single-File Web Applications

## Analisis
**Baris 11: `if __name__ == '__main__':`**
Cara Python menjalankan kode hanya ketika file dijalankan langsung (bukan di-import). Jadi kode di dalam blok ini hanya jalan waktu kita ketik python app.py

**Baris 12-14: Konfigurasi Pyramid**
Configurator menghubungkan URL (/) dengan fungsi view (hello_world). Jadi ketika ada request ke http://localhost:6543/, Pyramid tahu harus memanggil fungsi hello_world

**Baris 6-8: Implementasi View**
Fungsi yang menghasilkan response. Terima object request, return object Response yang berisi HTML.

**Baris 15-17: Publikasi WSGI App**
Waitress adalah HTTP server yang menjalankan aplikasi WSGI kita. 

## Extra Credit
**Mengapa menggunakan `print('Incoming request')` bukan `print 'Incoming request'`?**
Karena kode ini untuk Python 3. Di Python 3, print adalah fungsi (harus pakai kurung). Di Python 2, print adalah statement (tanpa kurung).

**Apa yang terjadi jika mengembalikan string HTML? Atau sequence of integers?**
Di String HTML Akan error. Pyramid mengharapkan object Response, bukan string mentah. Harus dibungkus: return Response('html string'). Pada sequence of integers Juga error, karena bukan tipe data yang valid untuk response HTTP.

**Exception Handling - Print xyz**
Waktu reload browser, akan muncul exception/error di console tempat kita menjalankan python app.py. Browser akan menampilkan error page atau tidak bisa load.

**GI dalam WSGI - Gateway Interface** 
Standard lama untuk menjalankan program di web server. WSGI adalah versi modern untuk Python yang lebih efisien dan fleksibel.