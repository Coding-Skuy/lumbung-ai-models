> Versi: v1.0.0 | Status: disetujui | Menggantikan: -
> Sumber: Lumbung-TownHall `platform/versions/v1.0.0/` pada commit `673a467` ([platform/versions/v1.0.0](https://github.com/Coding-Skuy/Lumbung-TownHall/blob/673a467126e195ffd67c9d3ff21d108193a6c3ec/platform/versions/v1.0.0))

# 40 — Tech Stack lumbung-ai-models

Matriks stack AI. Belum ada model terlatih; stack mengunci arah.

## Matriks

| Aspek | Keputusan |
|---|---|
| Training | Python, notebook eksperimen + skrip `training/` |
| Serving | Rust via API HTTP (internal, service key) |
| Artefak wajib | model card, metrik eval, versi model, hasil eval per rilis |
| Target v1 | LMB-AI-002 prediksi susut per komoditas; LMB-AI-003 prediksi harga 3 komoditas pilot |
| Ambang susut | cabai 6%, bawang 4%, kangkung 8% (sortir); susut jalan maks 2%/trip; total <5% |
| Data sumber | timbang ganda KOTOR/BERSIH, trip, 3 harga referensi mingguan (via pipeline) |
