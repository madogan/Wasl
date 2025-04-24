# 📚 Wasl

## 1. Summary
**Wasl** (Arabic: وصل — "connection") is an open-source, AI-assisted knowledge graph built from classical and modern Islamic texts. Centered on Arabic, and supported by Turkish and English translations, it links words across the Quran, Hadith, Tafsir, and classical dictionaries to uncover deep, contextual, and historical meanings of language used in divine and prophetic revelation.

## 2. Purpose
Wasl’s purpose is to build a **data-driven, multilingual dictionary of Islamic vocabulary** — not from assumptions, but from actual usage across centuries of texts. By analyzing how Arabic words are used in the Quran and Hadith, how scholars explained them in Tafsir and Luğat, and how their meanings evolved over time, Wasl helps us better understand what **Allah** says in the Quran and what the **Prophet ﷺ** meant in the Hadith.

## 3. Solution
Wasl creates a fully linked, AI-enriched dataset:
- Arabic at the center, translated into Turkish and English
- Word-to-root relationships + reverse mappings
- Historical dictionaries (luğat) with timeline-based word sense evolution
- Authenticity-tagged hadiths (ṣaḥīḥ, ḥasan, ḍaʿīf)
- Graph-based exploration in tools like Obsidian
- Contextual embeddings via **BERT/ArabicBERT** models

## 4. Tasks

### ✅ 1. Collection of Core Texts
- [x] Quran (Tanzil.net)
- [ ] Tafsir (Ibn Kathir, Tabari, etc.)
- [ ] Classical dictionaries (Lisan al-Arab, Taj al-Arus, etc.)
- [ ] Hadith (Bukhari, Muslim, Tirmidhi, Nasa’i, etc.)
- [ ] Classification data for hadiths (ṣaḥīḥ, ḥasan, ḍaʿīf)
- [ ] Modern Arabic texts for meaning evolution

### 📁 2. Obsidian File Structure
```
/Wasl/
├── books/               # Full original sources in .md (Quran, Hadith, etc.)
├── ayat/                # Each verse as a separate page
│   └── ayet_2.2.md
├── hadith/              # Each hadith entry individually stored
├── roots/               # Root index (e.g., root_س_ل_م.md)
│   └── kok_س_ل_م.md
│       ├── words/       # Words derived from root
│       │   └── word_مسلم.md
├── words/               # Every Arabic word with meaning & references
│   └── word_مسلم.md
├── analysis/            # Semantic stats, usage evolution, etc.
├── meta/                # Metadata, configs
```

### 🧠 3. Morphological & Semantic Processing
- Tokenization, root extraction using CAMeL Tools or Farasa
- Embedding with ArabicBERT for contextual analysis
- Manual + AI-supported definition tagging (Arabic, Turkish, English)

### 🔗 4. Relationship & Reference Structure
- `word_` → links to `root_`
- `root_` → lists all related `word_` entries
- `root_` → backlinks to `ayat_` and `hadith_` where used
- `ayat_` and `hadith_` pages → backlink to `root_` they contain
- `word_` → backlinks to `ayat_` and `hadith_` where used
- `ayat_` and `hadith_` pages → backlink to `word_` they contain
- Graph visualization via Obsidian’s native graph view

### 📊 5. Analytics
- First occurrence, most common chapter
- Semantic drift over centuries (dictionary + tafsir comparison)
- Word frequency and usage networks

## 🧭 Who Is This For?
- Scholars of Arabic, Tafsir, Hadith, and Islamic Studies
- NLP researchers focused on Arabic & Semitic languages
- Students seeking contextual understanding of Quranic and Prophetic vocabulary