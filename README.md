# AI-training-data-Intern
Digitization of 7 NCERT textbooks,text into latex and images into tikz .Raw text destroys the layout but latex turns  the textbooks into machine readable code.I was tasked with building a high precision dataset to train AI models.

 NCERT English Textbooks Digitization & Qdrant Vector DB Ingestion Pipeline

An end-to-end AI training data engineering pipeline designed to digitize 7 NCERT English textbooks into structured LaTeX markup and native TikZ vector graphics for high-precision Retrieval-Augmented Generation (RAG) systems and LLM fine-tuning.

---

 Project Overview

Raw OCR text extraction destroys visual hierarchy, sidebars, dialogue structures, and exercise formats, leading to context degradation and LLM hallucinations in EdTech applications. 

This project solves this challenge by systematically digitizing 7 NCERT English textbooks across 4 grade levels into machine-readable **LaTeX** environments (`tcolorbox`, `marginnote`, `verse`) and code-rendered **TikZ** visual artwork, followed by chunking, vector embedding, and metadata ingestion into a **Qdrant Vector Database**.

* **Organization:** Onespeer LLP
* **Role:** AI Training Data Intern
* **Intern:** M. Zeba Fathima
* **Roll No:** 20241CSE0373
* **Section:** CSE05

---

 Scope of Digitized Datasets (7 Textbooks)

| Grade Level | Textbook Name | Type | Key Content Processed |
| :--- | :--- | :--- | :--- |
| **Class 12** | *Flamingo* | Main Reader | Chapters 1–8 + 6 Poems |
| **Class 12** | *Vistas* | Supplementary Reader | Chapters 1–6 |
| **Class 11** | *Hornbill* | Main Reader | Chapters 1–8 + Poems |
| **Class 9** | *Beehive* | Main Reader | Chapters 1–11 + Poems |
| **Class 9** | *Moments* | Supplementary Reader | Chapters 1–10 |
| **Class 8** | *Honeydew* | Main Reader | Chapters 1–8 + Poems |
| **Class 8** | *It So Happened* | Supplementary Reader | Chapters 1–10 |

---

 Key Technical Contributions

1. **Semantic Layout Preservation:** 
   * Formatted continuous prose narratives into custom LaTeX markup.
   * Preserved poetic stanzas using the `verse` environment to prevent token bleeding.
   * Structured multi-speaker dialogues, callouts, and vocabulary margins using `marginnote` and `tcolorbox`.
   * Formatted exercise grids, fill-in-the-blanks, and tables using `tabular`, `colortbl`, and `xcolor`.

2. **Code-Rendered Visual Artwork (TikZ):**
   * Converted textbook illustrations, maps, and activity diagrams into native, compilable **TikZ vector graphics**.
   * Enabled vector databases to search and reason over visual graphics programmatically.

3. **Vector Database Ingestion (Qdrant):**
   * Chunked LaTeX source files into optimal semantic tokens.
   * Generated dense vector embeddings for text chunks and TikZ graphic blocks.
   * Attached granular metadata payloads (`grade`, `book_name`, `chapter`, `content_type`) to eliminate cross-grade search leakage during RAG retrieval.

---

