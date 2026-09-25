# Hybrid RAG + Fine-Tuning for Controlled Customer Support Generation

A controlled customer-support generation system that combines
Retrieval-Augmented Generation (RAG) with Parameter-Efficient Fine-Tuning
(PEFT) to generate accurate, context-aware, and policy-aligned responses.

## Project Overview

Customer-support LLMs can generate fluent responses that may not always
follow company policies or operational guidelines.

This project addresses that problem by combining:

- Retrieval-Augmented Generation (RAG)
- Corporate SOP / policy documents
- Semantic search
- Large Language Models
- LoRA / PEFT fine-tuning
- Automated evaluation

The system retrieves relevant information from a structured knowledge
base and combines it with a fine-tuned language model to improve
controlled customer-support response generation.

## Architecture

The system combines fine-tuned intent extraction with semantic retrieval
from a policy knowledge base before generating the final customer-support
response.

### Pipeline

User Query
   ↓
Fine-Tuned LLM
   ↓
Intent Extraction
   ↓
Semantic Retrieval
   ↓
Relevant SOP / Policy Context
   ↓
Response Generation
   ↓
Customer Support Response
   ↓
Evaluation

---

## Tech Stack

| Category | Technologies |
|---|---|
| Language | Python |
| LLM | Qwen2.5-1.5B-Instruct |
| RAG | LangChain |
| Embeddings | all-MiniLM-L6-v2 |
| Vector Database | ChromaDB |
| Fine-Tuning | LoRA / PEFT |
| Data Processing | Pandas, NumPy |
| ML | Scikit-learn |
| Evaluation | Custom evaluation pipeline |
| Environment | Google Colab / Jupyter |

---

## Dataset

The project uses the Bitext customer-support dataset for model
development and evaluation.

The RAG knowledge base consists of 13 SOP / policy documents used
as the grounding source for customer-support responses.

---

## Project Pipeline

### 1. Data Understanding & EDA

Exploration of the customer-support dataset, including:

- Dataset structure
- Intent distribution
- Category distribution
- Missing values
- Text characteristics

### 2. Data Preparation

- Data cleaning
- Sampling
- Train/validation/test split
- Tokenization
- Dataset preparation

### 3. Baseline Model

A baseline LLM is evaluated before introducing RAG and fine-tuning.

### 4. RAG Implementation

Relevant SOP documents are:

1. Loaded
2. Chunked
3. Embedded
4. Stored in ChromaDB
5. Retrieved based on semantic similarity

### 5. RAG Evaluation

The RAG-based system is evaluated against the baseline.

### 6. Fine-Tuning

Parameter-Efficient Fine-Tuning using LoRA is applied to adapt the
language model to the customer-support task.

### 7. Fine-Tuned RAG

The final system combines:

**Fine-Tuned LLM + RAG + SOP Knowledge Base**

and is compared with the baseline and RAG-only approaches.

---

## Results

The system was evaluated across three architectures:

| Architecture | ROUGE-1 | ROUGE-L | BLEU | Hallucination Rate | Retrieval Precision |
|---|---:|---:|---:|---:|---:|
| Baseline (Zero-Shot) | 0.295 | 0.190 | 0.014 | 35.0% | 0% |
| Solution V1 (Naive RAG) | 0.263 | 0.182 | 0.018 | 15.0% | 62.5% |
| Solution V2 (Hybrid RAG) | **0.301** | **0.219** | **0.047** | **3.5%** | **83.3%** |

The evaluated Hybrid RAG configuration achieved a measured hallucination
rate of 3.5% and retrieval precision of 83.3%, compared with 15.0% and
62.5% for the evaluated Naive RAG configuration.

Detailed evaluation results are available in:

`docs/Comparative_Analysis_Report.pdf`

## Repository Structure

```text
├── docs/
├── notebooks/
├── data/
├── results/
├── knowledge_base/
├── assets/
└── requirements.txt 
