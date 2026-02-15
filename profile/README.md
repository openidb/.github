<div align="right" dir="rtl">

**بسم الله الرحمن الرحيم**

الحمد لله ربّ العالمين، والصلاة والسلام على أشرف الأنبياء والمرسلين، نبيّنا محمّد وعلى آله وصحبه أجمعين.

قال رسول الله ﷺ:

> بَلِّغُوا عَنِّي وَلَوْ آيَةً، وَحَدِّثُوا عَنْ بَنِي إِسْرَائِيلَ وَلاَ حَرَجَ، وَمَنْ كَذَبَ عَلَىَّ مُتَعَمِّدًا فَلْيَتَبَوَّأْ مَقْعَدَهُ مِنَ النَّارِ
>
> — صحيح البخاري ٣٤٦١

> مَنْ دَعَا إِلَى هُدَى كَانَ لَهُ مِنَ الأَجْرِ مِثْلُ أُجُورِ مَنْ تَبِعَهُ لاَ يَنْقُصُ ذَلِكَ مِنْ أُجُورِهِمْ شَيْئًا
>
> — رياض الصالحين ١٣٨٢

> نَضَّرَ اللَّهُ امْرَأً سَمِعَ مِنَّا شَيْئًا فَبَلَّغَهُ كَمَا سَمِعَهُ فَرُبَّ مُبَلِّغٍ أَوْعَى مِنْ سَامِعٍ
>
> — رياض الصالحين ١٣٨٩

</div>

---

# OpenIslamicDB

Open-source database and API for Islamic texts — Quran, Hadith, classical Arabic books, and Arabic dictionaries — with hybrid search combining semantic similarity, keyword matching, knowledge graphs, and LLM reranking.

## Data

| Domain | Volume |
|--------|--------|
| **Quran** | 6,236 ayahs, 500+ translations (90+ languages), 27 tafsirs, 100+ audio reciters |
| **Hadith** | 166,964 hadiths across 24 collections, 67K+ English translations |
| **Books** | 8,500+ classical Arabic texts with full-text pages, PDFs, metadata |
| **Dictionary** | 43 dictionaries, 115K entries, 155K+ sub-entries, 457K root mappings |

## Repositories

| Repo | Description | Stack |
|------|-------------|-------|
| [**api**](https://github.com/openidb/api) | REST API server | Hono, PostgreSQL, Qdrant, Elasticsearch, Neo4j |
| [**frontend**](https://github.com/openidb/frontend) | Web frontend | Next.js 16, Tailwind CSS, shadcn/ui |
| [**scrapers**](https://github.com/openidb/scrapers) | Data acquisition docs | TypeScript pipelines (code lives in api/) |

## Data Sources

### Quran

| What | Source |
|------|--------|
| **Text** | [Al Quran Cloud API](https://alquran.cloud/) — Uthmani script (Hafs an Asim) |
| **Translations** | [fawazahmed0/quran-api](https://github.com/fawazahmed0/quran-api) — 500+ editions, 90+ languages |
| **Tafsirs** | [spa5k/tafsir_api](https://github.com/spa5k/tafsir_api) — 27 editions, 6 languages |
| **Audio** | [EveryAyah.com](https://everyayah.com/), [Al Quran Cloud CDN](https://cdn.islamic.network/), [Quran Foundation](https://quran.com/), [QUL / Tarteel AI](https://qul.tarteel.ai/) |

### Hadith

- **[sunnah.com](https://sunnah.com/)** — 17 collections (49,618 hadiths) with Arabic text and English translations
- **[hadithunlocked.com](https://hadithunlocked.com/)** — 7 collections (117,346 hadiths) with full tashkeel, isnad/matn separation, scholarly grading, and human-only English translations

### Books & Dictionaries

- **[Turath.io](https://turath.io/)** — 8,500+ classical Arabic texts and 43 Arabic dictionaries (same corpus as [Shamela.ws](https://shamela.ws/))
- **[Arramooz](https://github.com/linuxscout/arramooz)** — Arabic morphological database for root derivation
- **KhorsiCorpus** — Taj al-Arus word-root derivatives for morphological pattern generation

## Quick Start

```bash
# 1. Start infrastructure
cd api && docker compose up -d

# 2. Start API server
bun install && bun run dev          # http://localhost:4000

# 3. Start frontend (in another terminal)
cd ../frontend/web && bun install && bun run dev   # http://localhost:3000
```
