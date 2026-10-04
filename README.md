# lumbung-ai-models

Model AI Lumbung untuk hortikultura: prediksi susut dan prediksi harga.

## Ruang Lingkup

- Prediksi susut: selisih berat panen kebun vs berat terima gudang per lot dan trip.
- Prediksi harga: perkiraan harga per komoditas per pasar induk.

## Teknologi

- Python — training dan eksperimen (`notebooks/`, `training/` bila ada).
- Rust — serving model via API HTTP (endpoint di `lumbung-backend-service` atau layanan kecil di sini).

## Struktur

```text
lumbung-ai-models/
├── models/README.md      # daftar model tersimpan
├── notebooks/README.md   # eksperimen
└── training/             # skrip training (menyusul)
```

## Status Model

Belum ada model terlatih. Seluruh direktori berisi STUB jujur sampai data timbangan, trip, dan harga pasar induk tersedia.

## Keterkaitan

- Data: [lumbung-data-pipeline](https://github.com/Coding-Skuy/lumbung-data-pipeline)
- Backend serving: [lumbung-backend-service](https://github.com/Coding-Skuy/lumbung-backend-service)
