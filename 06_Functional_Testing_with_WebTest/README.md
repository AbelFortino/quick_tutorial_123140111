# 06: Functional Testing with WebTest

## Analisis
- Melakukan end-to-end pengujian fungsional (simulasi full HTTP request) untuk memverifikasi seluruh tumpukan aplikasi, termasuk templating dan respons HTML.
- Menggunakan webtest (dipasang sebagai dependensi [dev]).
- Tes berjalan cepat karena WebTest melewati setup server HTTP fisik, menjadikannya ideal untuk TDD (Test-Driven Development).
- Menggunakan self.testapp.get('/', status=200) untuk mensimulasikan permintaan HTTP GET ke root (/).
- Memeriksa konten HTML di respons (res.body) menggunakan self.assertIn(b'<h1>Hello World!</h1>', res.body).