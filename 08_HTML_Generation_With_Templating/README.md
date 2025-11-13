# 08: HTML Generation With Templating

## Analisis
- Memisahkan kode HTML dari Python, menggunakan templating.
- pyramid_chameleon diinstal dan di-include (config.include) sebagai renderer.
- Fungsi view tidak lagi mengembalikan objek Response berisi HTML, tetapi hanya mengembalikan Kamus (data Python).
- @view_config(renderer='home.pt') mengaitkan data yang dikembalikan oleh view dengan template home.pt.
- File .pt (Chameleon) menyisipkan data menggunakan sintaks seperti ${name}.
- Unit test kini memeriksa data yang dikembalikan oleh view, bukan response HTTP.
- Opsi pyramid.reload_templates = true di .ini memastikan template dimuat ulang secara otomatis.