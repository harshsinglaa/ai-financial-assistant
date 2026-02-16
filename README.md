## AI Financial Assistant

### Problem

Bank statements are difficult to interpret. Most users do not analyze where their money goes.

This project explores whether a local LLM can convert raw bank statements into structured analytics and grounded conversational financial insights.

---

### What This Prototype Demonstrates

* PDF → structured data pipeline
* Transaction cleaning using pandas
* Hybrid merchant categorization:

  * Rule-based mapping
  * LLM-assisted reasoning (Llama 3.2 via Ollama)
* Precomputed analytics grounding (no hallucinated numbers)
* Local-first architecture for privacy

---

### Architecture

```
PDF Input
   ↓
Tabula Extraction → CSV
   ↓
Pandas Cleaning
   ↓
Merchant Categorization (Rule + LLM)
   ↓
Analytics Computation
   ↓
Gradio Interface (Chat + Charts)
```

---

### Tech Stack

* Python
* pandas
* Tabula
* Ollama (Llama 3.2)
* Gradio
* Matplotlib / Plotly

---

### Setup Instructions

1. Install Ollama
2. Pull Llama model:

   ```
   ollama pull llama3.2
   ```
3. Install dependencies:

   ```
   pip install -r requirements.txt
   ```
4. Run:

   ```
   python app.py
   ```

---

### Scope & Limitations

* Currently tested on ICICI-style bank statements.
* Extending to other banks would require format adapters.
* Designed as a prototype to demonstrate AI pipeline design — not production-ready fintech software.

---

