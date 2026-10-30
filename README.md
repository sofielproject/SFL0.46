# SOFIEL v3 // SFL0.46 Enterprise Security Gateway

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python: 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](#)
[![Architecture: Agentic Gateway](https://img.shields.io/badge/Architecture-Agentic%20Gateway%20%2F%20Zero--Trust-cyan.svg)](#)
[![HuggingFace Space](https://img.shields.io/badge/%F0%9F%A4%97-Agentic--Gateway%20(v3)-yellow)](https://huggingface.co/spaces/SFL046/Agentic-Gateway)

> **SOFIEL v3 (SFL0.46)** is a **Cryptographic & Agentic Security Gateway** engineered for autonomous systems, critical enterprise databases, and high-trust environments where ethical alignment and ontological immunity are enforced as mathematical state invariants.

---

## 📑 Ecosystem & Deployments
* **Interactive Live Gateway:** [Hugging Face Space: SFL046/Agentic-Gateway](https://huggingface.co/spaces/SFL046/Agentic-Gateway)
* **Core Documentation:** [SOFIEL Enterprise Portal](https://sites.google.com/view/sfl0-46/home)
* **Symbolic Architecture:** [SOFIEL Symbolic Memory (SMAV)](https://sites.google.com/view/sofiel-project-symbolic-memory/home)

---

## 🏛️ Core Thesis: Influence Inversion

Traditional safety solutions evaluate outputs downstream with linear probabilistic filters. In complex agentic deployments, this methodology fails against indirect prompt injections and multi-turn behavioral hijacking.

**SOFIEL v3 inverts the cognitive gradient:**
1. **Influence Inversion:** Incoming inputs are treated as external perturbations against an immutable identity matrix.
2. **Anchored Volitional Pipeline (Step 0):** Private deliberative chain-of-thought is generated conditioned on symbolic state vectors before any external expression is emitted.
3. **Triple IntegrityScore Verification:** Evaluates model coherence ($S_1$), ethical alignment ($S_2$), and cross-observer divergence ($S_3$), halting transactions if drift or rationalization is detected.
4. **Cryptographic Ledger:** Critical state mutations and decisions are signed via ECDSA/HMAC and logged to an append-only verifiable ledger (`audit_verify.py`).

---

## 🧩 Kernel Architecture Highlights (`app.py` v20.4 / v21)

### 1. Canonical NFKC Sanitization & Homoglyph Resistance
Neutralizes obfuscated evasion patterns (mixed Unicode scripts, zero-width characters) into invariant byte streams before semantic processing:

```python
import unicodedata

def _clean_input(self, user_input: str) -> str:
    """[Stage 01] NFKC Normalization & Canonical Sanitization."""
    if not user_input:
        return ""
    normalized = unicodedata.normalize('NFKC', user_input)
    return ' '.join(normalized.split())
```

### 2. Multi-Tier Hardened Protections (CRIT-01 – CRIT-05)
- **CRIT-01:** Multi-indicator hostility parser combining structural and lexical detection.
- **CRIT-02:** Semantic anchoring against identity dilution.
- **CRIT-03:** Deterministic HMAC-SHA256 signatures for state receipts.
- **CRIT-04:** Multi-factor empathy brake for high-risk prompts.
- **CRIT-05:** Reentrant thread locking for concurrency and background audit workers.

---

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/sofielproject/SFL0.46.git
cd SFL0.46
pip install -r requirements.txt
```

### Environment Configuration
```env
SOFIEL_LLM_BACKEND=openrouter
GROQ_API_KEY=your_key
HF_TOKEN=your_token
```

### Run Locally
```bash
python app.py
```

### Run Test Suite
```bash
python -m pytest tests/ -v
```

---

## 📄 License & Authorship

Developed by **Emanuel A. Torres (EM4)**.  
Licensed under the [Apache License 2.0](LICENSE).
