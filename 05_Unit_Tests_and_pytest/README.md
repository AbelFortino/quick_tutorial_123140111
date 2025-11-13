# 05: Unit Tests and pytest

## Analisis
- Memastikan kode Python bekerja dengan benar ("Untested code is broken code"), lebih efisien daripada browser reload saat pengembangan.
- Menggunakan pytest (dipasang sebagai dependensi [dev]) sebagai test runner pilihan di Pyramid.
- Setiap tes harus terisolasi (unit)—misalnya, dengan mengimpor fungsi view di dalam fungsi tes itu sendiri.
- Tes membuat testing.DummyRequest() palsu, memanggil view (hello_world), dan memverifikasi response.status_code (memastikan hasilnya 200).