# Open Islamic Database (OpenIDB)

Open-source infrastructure for Islamic texts — Quran, Hadith, classical Arabic books, and Arabic dictionaries. Structured data with REST APIs, hybrid search, and knowledge graphs.

## Repositories

### [openidb](https://github.com/openidb/openidb) — REST API & Search Engine

Hono REST API backed by PostgreSQL, Qdrant, Elasticsearch, and Neo4j. Serves Quran (6,236 ayahs, 500+ translation editions across 90+ languages, 27 tafsirs in 6 languages), Hadith (17 collections, 49,618 hadiths), classical Arabic books from [Turath.io](https://turath.io/), and Arabic dictionaries (43 sources, ~115K entries, 155K+ sub-entries with root derivation).

REST endpoints: `/api/search`, `/api/quran`, `/api/hadith`, `/api/books`, `/api/books/authors`, `/api/books/categories`, `/api/dictionary`, `/api/transcribe`, `/api/stats`, `/api/health`.

Search combines semantic similarity (Gemini embeddings via Qdrant) with keyword matching (Elasticsearch BM25) using Reciprocal Rank Fusion, Neo4j knowledge graph context, LLM reranking, and query expansion.

### [sabeel](https://github.com/openidb/sabeel) — Frontend

Next.js app with hybrid search UI, HTML book reader with inline word definitions, voice input, knowledge graph panel, and dark mode. Supports 13 interface languages with full RTL support. Consumes the openidb API.

**Live:** [sabeel.dev](https://sabeel.dev)

### [scrapers](https://github.com/openidb/scrapers) — Data Acquisition

TypeScript import pipelines for sourcing data from [Turath.io](https://turath.io/), sunnah.com, and multiple Quran APIs. Includes dictionary extraction (regex-based and LLM-based), root derivation from Arramooz and Taj al-Arus, and structured database imports.
