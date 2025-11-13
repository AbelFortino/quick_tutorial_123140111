# 03: Application Configuration with .ini Files

## Analisis
- development.ini: File konfigurasi utama, dibaca oleh pserve.
- Startup Berbasis Entry Point: .ini mengarahkan pserve untuk mencari entry point di setup.py, yang kemudian memanggil fungsi main di tutorial/__init__.py untuk membuat aplikasi WSGI.
- Konfigurasi Ganda: Mengatur aplikasi dan server (Waitress) termasuk port (localhost:6543).
- --reload: Opsi penting yang membuat aplikasi otomatis restart saat kode diubah selama pengembangan.