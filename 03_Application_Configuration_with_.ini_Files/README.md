# 03: Application Configuration with .ini Files

## Analisis
- File konfigurasi utama, dibaca oleh pserve.
- .ini mengarahkan pserve untuk mencari entry point di setup.py, yang kemudian memanggil fungsi main di tutorial/__init__.py untuk membuat aplikasi WSGI.
- Mengatur aplikasi dan server (Waitress) termasuk port (localhost:6543).
- Opsi penting yang membuat aplikasi otomatis restart saat kode diubah selama pengembangan.