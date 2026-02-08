# Open Islamic Database (OpenIDB)

Open-source infrastructure for Islamic texts — Quran, Hadith, and classical Arabic books. Structured data with full-text and semantic search.

## Repositories

### [openidb](https://github.com/openidb/openidb) — Database & API

Hono REST API backed by PostgreSQL, Qdrant, Elasticsearch, and Neo4j. Serves Quran (6,236 ayahs, 12 translation languages, 2 tafsirs), Hadith (17 collections, ~76,000 hadiths), and classical Arabic books from Shamela.ws.

### [sabeel](https://github.com/openidb/sabeel) — Search Frontend

Next.js frontend with hybrid search — combines semantic search (Gemini embeddings via Qdrant) with keyword search (Elasticsearch BM25) using Reciprocal Rank Fusion, plus LLM reranking and query expansion.

### [scrapers](https://github.com/openidb/scrapers) — Data Acquisition

Python and TypeScript scrapers for sourcing data from shamela.ws, sunnah.com, and multiple Quran APIs. Produces EPUB3 books, WARC archives, and structured database imports.
