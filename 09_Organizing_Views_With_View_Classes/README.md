# 09: Organizing Views With View Classes

## Analisis
- Mengelompokkan fungsi view yang terkait menjadi metode di dalam sebuah kelas untuk sentralisasi dan berbagi (sharing) konfigurasi/state.
- Menggunakan decorator @view_defaults(renderer='home.pt') di tingkat kelas untuk menetapkan konfigurasi renderer yang sama untuk semua metode view di kelas tersebut.
- Mengurangi pengulangan konfigurasi (renderer) dan mengelompokkan logika terkait secara logis.