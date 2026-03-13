---
title: Best Models for Business
nav_order: 2
---

# Best Models for Business

Open-source models that deliver real value for common business tasks — and run on affordable hardware.

---

## Quick Reference

| Model | Size | VRAM (4-bit) | VRAM (8-bit) | Est. tok/s (V100) | Best For |
|-------|------|--------------|--------------|-------------------|----------|
| **Llama 3.2 3B** | 3B | 2.5 GB | 4 GB | 80-100 | Simple tasks, chatbots, classification |
| **Mistral 7B** | 7B | 5 GB | 8 GB | 50-70 | General purpose, balanced performance |
| **Llama 3.1 8B** | 8B | 6 GB | 10 GB | 45-60 | General purpose, excellent instruction following |
| **Gemma 2 9B** | 9B | 7 GB | 11 GB | 40-55 | Enterprise tasks, structured output |
| **Qwen 2.5 14B** | 14B | 10 GB | 16 GB | 25-35 | Coding, reasoning, multilingual |
| **Mistral NeMo 12B** | 12B | 9 GB | 14 GB | 30-40 | Long context, document analysis |
| **Qwen 2.5 Coder 7B** | 7B | 5 GB | 8 GB | 50-70 | Code generation, debugging |
| **Qwen 2.5 Coder 32B** | 32B | 22 GB | 36 GB | 12-18 | Professional coding, complex reasoning |
| **Mixtral 8x7B** | 47B* | 24 GB | 45 GB | 15-25 | High-quality output, MoE efficiency |
| **Llama 3.3 70B** | 70B | 40 GB | 75 GB | 5-8 | Complex reasoning, premium quality |

*Mixtral uses Mixture of Experts: 47B total params, ~13B active per token

---

## Business Use Cases

### 1. Customer Support & Chatbots

**Recommended:** Mistral 7B, Llama 3.1 8B, Gemma 2 9B

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| Response quality | Good | Excellent |
| Speed needed | 30+ tok/s | 50+ tok/s |
| VRAM | 8 GB | 16 GB |

**What it does:**
- Answer FAQs
- Route tickets
- Draft responses
- Handle common queries 24/7

---

### 2. Document Summarization

**Recommended:** Mistral NeMo 12B, Llama 3.1 8B, Gemma 2 9B

| Document Size | Model | VRAM |
|---------------|-------|------|
| Short (<4K tokens) | Mistral 7B | 8 GB |
| Medium (4K-16K) | Mistral NeMo 12B | 16 GB |
| Long (16K-128K) | Llama 3.1 8B | 16 GB |

**What it does:**
- Summarize reports, emails, contracts
- Extract key points from meetings
- Create executive summaries

---

### 3. Translation & Localization

**Recommended:** Qwen 2.5 14B, Llama 3.1 8B

| Languages | Model | Notes |
|-----------|-------|-------|
| EN/DE/FR/ES | Llama 3.1 8B | Good for European languages |
| 30+ languages | Qwen 2.5 14B | Excellent multilingual support |
| Technical docs | Qwen 2.5 14B | Better at preserving terminology |

**What it does:**
- Translate documents, emails, websites
- Localize content for markets
- Real-time translation assistance

---

### 4. Code Generation & Review

**Recommended:** Qwen 2.5 Coder 7B, Qwen 2.5 Coder 32B

| Task | Model | VRAM | Quality |
|------|-------|------|---------|
| Simple functions | Qwen 2.5 Coder 7B | 8 GB | ⭐⭐⭐⭐ |
| Bug fixes | Qwen 2.5 Coder 7B | 8 GB | ⭐⭐⭐⭐ |
| Code review | Qwen 2.5 Coder 14B | 12 GB | ⭐⭐⭐⭐⭐ |
| Complex refactoring | Qwen 2.5 Coder 32B | 24 GB | ⭐⭐⭐⭐⭐ |
| Architecture decisions | Qwen 2.5 Coder 32B | 24 GB | ⭐⭐⭐⭐⭐ |

**What it does:**
- Generate code from descriptions
- Debug and fix errors
- Write tests
- Explain code
- Refactor legacy code

---

### 5. Content Writing & Marketing

**Recommended:** Llama 3.1 8B, Mistral 7B, Gemma 2 9B

| Content Type | Model | Why |
|--------------|-------|-----|
| Social media posts | Mistral 7B | Fast, creative |
| Blog articles | Llama 3.1 8B | Better structure |
| Email campaigns | Gemma 2 9B | Professional tone |
| Product descriptions | Llama 3.1 8B | Consistent quality |

**What it does:**
- Draft marketing copy
- Write blog posts
- Create social media content
- Generate email templates

---

### 6. Data Analysis & Reporting

**Recommended:** Llama 3.1 8B, Qwen 2.5 14B

| Task | Model | Speed | Quality |
|------|-------|-------|---------|
| SQL generation | Qwen 2.5 Coder 7B | Fast | ⭐⭐⭐⭐ |
| Data interpretation | Qwen 2.5 14B | Medium | ⭐⭐⭐⭐⭐ |
| Report writing | Llama 3.1 8B | Fast | ⭐⭐⭐⭐ |
| Chart descriptions | Gemma 2 9B | Fast | ⭐⭐⭐⭐ |

**What it does:**
- Generate SQL queries
- Interpret data patterns
- Write analysis reports
- Create data summaries

---

## Performance Requirements

### Tokens/Second Guidelines

| Use Case | Minimum | Comfortable | Excellent |
|----------|---------|-------------|-----------|
| Chatbot | 20 tok/s | 40 tok/s | 60+ tok/s |
| Document processing | 15 tok/s | 30 tok/s | 50+ tok/s |
| Batch processing | 10 tok/s | 20 tok/s | 40+ tok/s |
| Real-time assistance | 30 tok/s | 50 tok/s | 80+ tok/s |

**Human reading speed:** ~250 words/minute = ~4 words/second ≈ 5-6 tok/s

### Latency vs Throughput

- **Latency (TTFT):** Time to first token — important for chatbots
- **Throughput:** Total tokens/second — important for batch processing

| Hardware | 7B model tok/s | 14B model tok/s | 70B model tok/s |
|----------|----------------|-----------------|-----------------|
| Tesla P100 | 35-50 | 15-25 | 3-6 |
| Tesla V100 | 50-70 | 25-40 | 5-10 |
| Tesla T4 | 30-45 | 12-20 | 3-5 |
| 2x V100 | 90-120 | 45-70 | 10-18 |

---

## Model Selection by Budget

### Under €2,000 (2x P100, 32GB VRAM total)

```
✅ Mistral 7B (fast, reliable)
✅ Llama 3.1 8B (great instruction following)
✅ Qwen 2.5 Coder 7B (coding)
✅ Gemma 2 9B (enterprise tasks)
⚠️ Qwen 2.5 14B (tight fit, single GPU)
❌ Mixtral, 70B models
```

### €3,000-5,000 (2x V100 16GB or 2x T4, 32GB VRAM)

```
✅ All models from above (faster)
✅ Qwen 2.5 14B (comfortable)
✅ Qwen 2.5 Coder 32B (tight fit)
⚠️ Mixtral 8x7B (quantized, slow)
❌ 70B models
```

### €6,000-8,000 (2x V100 32GB, 64GB VRAM)

```
✅ All smaller models (very fast)
✅ Qwen 2.5 Coder 32B (comfortable)
✅ Mixtral 8x7B (good speed)
⚠️ Llama 3.3 70B (4-bit, usable)
```

---

## Our Recommendations

### Best All-Rounder
**Llama 3.1 8B** — Excellent instruction following, good at most tasks, fits on any GPU.

### Best for Coding
**Qwen 2.5 Coder 32B** — Matches GPT-4 on coding benchmarks. Needs 24GB+ VRAM.

### Best for Multilingual
**Qwen 2.5 14B** — Supports 30+ languages, great translation quality.

### Best for Documents
**Mistral NeMo 12B** — 128K context window, excellent for long documents.

### Best Budget Option
**Mistral 7B** — Punches above its weight, very fast, runs on anything.

---

## Getting Started

All models are available through:

- **Ollama:** `ollama run llama3.1:8b`
- **vLLM:** Production-grade serving
- **llama.cpp:** Lightweight, CPU+GPU hybrid

We pre-install and configure these on all our servers.

---

[← Back to localai](/localai/)
