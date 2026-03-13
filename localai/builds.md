---
title: Build Configurations
nav_order: 4
---

# Build Configurations

Recommended server configurations for different budgets and workloads.

---

## Budget Build: €1,500-2,000

**Target:** Small businesses, experimentation, light inference workloads

| Component | Spec | Est. Price |
|-----------|------|------------|
| GPU | 2x Tesla P100 16GB | €600-800 |
| Server Chassis | Used Dell/HP/Supermicro 2U | €300-500 |
| CPU | Xeon E5-26xx (included) | — |
| RAM | 64GB DDR4 ECC | €150-200 |
| Storage | 1TB NVMe SSD | €100-150 |
| **Total** | | **€1,150-1,650** |

**What it runs:**
- LLaMA 2 7B, 13B (full precision)
- Mistral 7B
- Code models (CodeLlama 7B/13B)
- Stable Diffusion (slow but works)

---

## Value Build: €3,000-4,000

**Target:** Production inference, multiple concurrent users

| Component | Spec | Est. Price |
|-----------|------|------------|
| GPU | 2x Tesla V100 16GB | €1,600-2,400 |
| Server Chassis | Used Dell/HP/Supermicro 2U | €400-600 |
| CPU | Xeon Silver/Gold (included) | — |
| RAM | 128GB DDR4 ECC | €300-400 |
| Storage | 2TB NVMe SSD | €200-300 |
| **Total** | | **€2,500-3,700** |

**What it runs:**
- All models from Budget Build (faster)
- LLaMA 2 13B with context extensions
- Mixtral 8x7B (quantized)
- Multiple concurrent inference requests

---

## Efficiency Build: €3,500-5,000

**Target:** Always-on inference, low power consumption, quiet operation

| Component | Spec | Est. Price |
|-----------|------|------------|
| GPU | 2x Tesla T4 16GB | €3,000-4,000 |
| Server/Workstation | Quiet tower or 2U | €500-800 |
| CPU | Xeon or Ryzen (included) | — |
| RAM | 64-128GB DDR4 | €200-400 |
| Storage | 1-2TB NVMe SSD | €150-250 |
| **Total** | | **€3,850-5,450** |

**Why this build:**
- Only 70W per GPU — no special power requirements
- Can run in office environments (quiet)
- Excellent for INT8 inference workloads
- Easy to scale to 4 GPUs

---

## Performance Build: €6,000-8,000

**Target:** Larger models, heavier workloads

| Component | Spec | Est. Price |
|-----------|------|------------|
| GPU | 2x Tesla V100 32GB | €4,000-5,000 |
| Server Chassis | Quality 2U/4U | €600-1,000 |
| CPU | Dual Xeon Gold | €400-600 |
| RAM | 256GB DDR4 ECC | €600-800 |
| Storage | 4TB NVMe RAID | €400-600 |
| **Total** | | **€6,000-8,000** |

**What it runs:**
- LLaMA 2 70B (quantized 4-bit)
- LLaMA 3 70B (quantized)
- Large context windows
- Multi-model serving

---

## What's Included

All builds include:

- ✅ Pre-installed software stack (Ollama, vLLM, or custom)
- ✅ Model downloads and configuration
- ✅ Network setup and API endpoints
- ✅ Basic monitoring dashboard
- ✅ 30-day setup support

---

[← Back to localai](/localai/)
