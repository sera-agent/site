---
title: Hardware Options
---

# Hardware Options

We use proven NVIDIA Tesla datacenter GPUs — reliable, widely supported, and affordable on the refurbished market.

---

## GPU Comparison

| GPU | VRAM | Architecture | Tensor Cores | TDP | Used Price (est.) | Best For |
|-----|------|--------------|--------------|-----|-------------------|----------|
| **Tesla P100** | 16GB HBM2 | Pascal | — | 250W | €200-400 | Budget builds, models up to 13B |
| **Tesla V100** | 16GB HBM2 | Volta | 640 | 300W | €800-1,200 | Balanced performance |
| **Tesla V100** | 32GB HBM2 | Volta | 640 | 300W | €2,000-3,000 | Larger models (30B+) |
| **Tesla T4** | 16GB GDDR6 | Turing | 320 | 70W | €1,500-2,500 | Low power, efficient inference |
| **Tesla A100** | 40GB HBM2e | Ampere | 6,912 | 400W | €8,000+ | Premium builds (over budget) |

---

## Detailed Specs

### Tesla P100 (Pascal)
- **Launched:** 2016
- **Performance:** ~21 TFLOPS FP16
- **Memory Bandwidth:** 732 GB/s (HBM2)
- **Form Factor:** PCIe 3.0 x16
- **Notes:** Oldest viable option. No Tensor Cores, but excellent value. Great for learning and experimentation.

### Tesla V100 (Volta)
- **Launched:** 2017
- **Performance:** ~125 TFLOPS (Tensor), ~15 TFLOPS FP64
- **Memory Bandwidth:** 900 GB/s (HBM2)
- **Form Factor:** PCIe 3.0 or SXM2
- **Notes:** First GPU with Tensor Cores. Excellent for inference and light training. 32GB version fits larger models.

### Tesla T4 (Turing)
- **Launched:** 2018
- **Performance:** ~65 TFLOPS (Tensor INT8)
- **Memory Bandwidth:** 320 GB/s (GDDR6)
- **TDP:** Only 70W — no extra power cables needed
- **Notes:** Extremely power efficient. Ideal for always-on inference servers. Multi-GPU setups easy due to low power.

### Tesla A100 (Ampere)
- **Launched:** 2020
- **Performance:** ~312 TFLOPS (Tensor BF16)
- **Memory Bandwidth:** 1,555 GB/s (HBM2e)
- **Notes:** Current flagship. Excellent but expensive. Only viable in premium builds.

---

## Memory Requirements by Model Size

| Model Size | Min VRAM | Recommended VRAM |
|------------|----------|------------------|
| 7B parameters | 6GB | 8GB |
| 13B parameters | 12GB | 16GB |
| 30B parameters | 24GB | 32GB |
| 70B parameters | 48GB | 80GB (2x40GB or 1x80GB) |

**Note:** Using quantization (4-bit, 8-bit) can significantly reduce memory requirements.

---

[← Back to localai](/localai/)
