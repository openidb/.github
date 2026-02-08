# Open Islamic Database (OpenIDB)

Open-source infrastructure for Islamic texts — Quran, Hadith, and classical Arabic books. Structured data with hybrid search and knowledge graphs.

## Repositories

### [openidb](https://github.com/openidb/openidb) — Database & API

Hono REST API backed by PostgreSQL, Qdrant, Elasticsearch, and Neo4j. Serves Quran (12 translation languages, 2 tafsirs), Hadith (17 collections), and classical Arabic books extracted from Maktaba Shamela.

APIs: search, quran, hadith, books, authors, categories, transcription, and stats.

Search combines semantic similarity (Gemini embeddings via Qdrant) with keyword matching (Elasticsearch BM25) using Reciprocal Rank Fusion, Neo4j knowledge graph context, LLM reranking, and query expansion.

### [sabeel](https://github.com/openidb/sabeel) — Frontend

Next.js app with search UI, EPUB book reader, and voice input. Consumes the openidb API.

### [scrapers](https://github.com/openidb/scrapers) — Data Acquisition

Python and TypeScript scrapers for sourcing data from Maktaba Shamela, sunnah.com, and multiple Quran APIs. Produces EPUB3 books, WARC archives, and structured database imports.
