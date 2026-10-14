# ADR-0001 — Fondasi teknis lumbung-ai-models

- Status: Diterima
- Tanggal: 2026-10-14

## Konteks

lumbung-ai-models berisi prediksi susut dan prediksi harga. Belum ada model terlatih; README mencatat direktori sebagai stub sampai data timbangan/trip/harga tersedia.

## Keputusan

1. Training dalam Python; serving hanya lewat API Rust. Tidak ada Python di jalur produksi.
2. Setiap model wajib model card + metrik eval + versi model; rilis diblokir bila QA gate gagal.
3. Cakupan v1.0.0: 3 komoditas pilot (cabai, bawang, kangkung); prediksi harga 12 komoditas milik Titeny, bukan repo ini (KONTEKS §4).
4. Data masuk hanya dari `lumbung-data-pipeline`; model tidak menulis ke DB `lumbung` dan tidak menyentuh DB divisi lain.
5. Serving memakai service key (`X-Service-Key`, least privilege: baca agregat); perubahan kontrak serving = ADR + bump versi.

## Konsekuensi

- Tidak ada klaim akurasi di dokumen sebelum metrik eval tercatat.
- Ambang alarm susut mengikuti BRD; perubahan ambang = PR requirement di TownHall dulu.
