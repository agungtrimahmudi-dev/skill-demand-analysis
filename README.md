# Skill Demand Analysis

Analisis mingguan permintaan skill di pasar kerja dari data lowongan kerja LinkedIn (4 minggu terakhir). Membandingkan demand industri terhadap skill terverifikasi pemilik, lalu menghasilkan:

- **`skill_gap_report.md`** — 30 skill paling banyak diminta, gap prioritas, dan korelasi antar-skill
- **`project_ideas.md`** — ide proyek konkret untuk menutup gap dan memperdalam kekuatan
- **`learning_plan.md`** — roadmap belajar 12 minggu berbasis proyek

## Hasil Analisis Terbaru

*Generated: 2026-08-10 — 329 lowongan dianalisis*

| Peringkat | Skill | Demand | % Lowongan | Dimiliki |
|-----------|-------|--------|------------|----------|
| 1 | n8n workflow SDK (TypeScript) | 230 | 69.9% | ✅ |
| 2 | API contract design | 203 | 61.7% | ✅ |
| 3 | RAG | 192 | 58.4% | ✅ |
| 4 | n8n | 139 | 42.2% | ✅ |
| 5 | Java | 136 | 41.3% | ✅ |
| 6 | Git | 129 | 39.2% | ✅ |
| 7 | Prompt engineering | 121 | 36.8% | ✅ |
| 8 | Browser automation (Playwright) | 113 | 34.3% | ✅ |
| 9 | ETL / normalisasi data multi-sumber | 110 | 33.4% | ✅ |
| 10 | FastAPI | 108 | 32.8% | ✅ |

**Gap yang perlu ditutup:** CI/CD (13.1%), Azure (10.6%).

**Pola pasar:** lowongan Automation/AI Engineer dominan meminta kombinasi *RAG + n8n + API contract design + prompt engineering* — 58% lowongan menyebut RAG, dan pasangan skill paling umum adalah `n8n workflow SDK ↔ RAG` (186 lowongan).

## Cara Menjalankan

```bash
# Prasyarat: Python 3.11+, data scrape di data/processed/jobs_matched/matched_*.json
python tools/skill_demand_analyzer.py
```

Skrip membaca skill terverifikasi dari `USER_SKILLS.md`, mengambil semua lowongan dari 4 minggu terakhir, menghitung frekuensi + korelasi skill, lalu menghasilkan 3 laporan di `skill_demand_analysis/`.

## Struktur

```
skill-demand-analysis/
├── skill_gap_report.md   # demand vs skill, gap, co-occurrence
├── project_ideas.md      # proyek untuk menutup gap & memperdalam kekuatan
└── learning_plan.md      # roadmap 12 minggu berbasis proyek
```

## Catatan Metodologi

- Data: lowongan yang di-scrape dari LinkedIn dan di-match otomatis (field `required_skills`, `nice_to_have_skills`, `top_matches`)
- Matching skill pemilik: substring/core-keyword match terhadap `USER_SKILLS.md` (39 skill terverifikasi) + baseline CS
- Analisis hanya melihat 4 minggu terakhir agar relevan dengan tren pasar saat ini

## Lisensi

MIT © 2026 Agung Trimahmudi
