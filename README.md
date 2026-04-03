# AI Underwriting Assistant (Production System)

## 🚀 Problem

Life insurance underwriting is document-heavy and time-consuming.

- 10–15 documents per application  
- ~20 pages per document  
- Manual review slows decision-making  

👉 Goal: Automate document understanding and assist underwriters with structured insights.

---

## 🧠 System Overview

End-to-end AI system that processes documents and generates summaries.

### Flow:

Documents → OCR → Classification → Rule Engine → LLM Summary → UI

---

## ⚙️ Tech Stack

- OCR: Azure Document Intelligence  
- LLM: GPT-4.1  
- Embeddings: BAAI/bge-m3  
- Reranker: bge-reranker-v2-m3  
- Hosting: Azure Kubernetes Service (AKS)  

---

## 🔄 System Design

### Stage 1: Preprocessing
- OCR extraction  
- Document classification  
- Rule retrieval  

### Stage 2: On-Demand Processing
- Triggered via “Generate Summary”  
- LLM generates structured output  

---

## ⚖️ Key Design Decisions

### Full Context vs RAG
- Started with full document context  
- RAG planned for optimization  

### Hybrid Rule + LLM
- Rules handle deterministic checks  
- LLM handles interpretation  

---

## 📊 Scale

- ~600 applications/month  
- 10–15 documents per case  
- ~3 LLM calls per document  

---

## ⚠️ Challenges

- OCR inconsistencies  
- Hallucination risk  
- Latency vs cost tradeoffs  

---

## 📈 Learnings

- LLMs require guardrails in production  
- Hybrid systems outperform pure LLMs  
- Evaluation is critical  

---

## 👩‍💼 My Role

- Coordinated between business, vendor, and engineering  
- Defined tradeoffs (cost vs accuracy vs latency) 

---

## 🔗 Related

(UI repo link to be added)
