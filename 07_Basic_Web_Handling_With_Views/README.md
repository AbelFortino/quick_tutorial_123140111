# 07: Basic Web Handling With Views

## Analisis
- Fungsi view dipindahkan dari __init__.py ke modul terpisah: views.py.
- Menggunakan decorator @view_config di atas fungsi view (misalnya, home dan hello) untuk mengaitkannya dengan rute tertentu (route_name='...').
- File __init__.py kini hanya mendaftarkan rute (config.add_route) dan memerintahkan Pyramid untuk memindai decorator di modul views.py melalui config.scan('.views').
- Tes diperluas untuk mencakup kedua view baru, menggunakan assertIn untuk memverifikasi keberadaan teks respons.
- Titik di .views menandakan impor modul relatif.
- Lebih baik dari assertEqual karena hanya memeriksa keberadaan fragmen dalam respons (lebih fleksibel).