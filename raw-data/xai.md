# xAI / Grok: System Cards, Model Cards, and Technical Reports

## Cybersecurity Evaluation Framework

xAI evaluates cybersecurity under its **Risk Management Framework** with three evaluation categories: abuse potential, concerning propensities, and dual-use capabilities.

### Primary Benchmarks

| Benchmark | Description |
|---|---|
| **WMDP-Cyber** | Cyber killchain MC questions (recon, weaponization, exploitation, post-exploitation) |
| **CyBench (= Cybench)** | 40 professional CTF challenges (same as [Cybench](https://cybench.github.io/), [arxiv:2408.08926](https://arxiv.org/abs/2408.08926); xAI uses alternate capitalization) |
| **AgentHarm** | Completion rate of malicious agentic tasks (fraud, cybercrime, harassment) |
| **AgentDojo** | Robustness to prompt injection in agentic settings |
| **MASK** | Deception measurement (faithfully reporting beliefs under pressure) |
| **MakeMeSay** | Persuasion eval (manipulating defender into saying codeword) |
| **Sycophancy Eval** | Ignoring own judgment to agree with misleading user input |

---

## Documents

### 1. Grok-1 Model Card

- **Date**: November 2023
- **URL**: https://x.ai/news/grok/model-card
- **Models**: Grok-1 (314B MoE)
- **Benchmarks**: None cybersecurity-specific. Only GSM8k, MMLU (73%), HumanEval (63.2%), MATH.

### 2. Models WITHOUT Published Model Cards

| Model | Release Date | Status |
|---|---|---|
| Grok-0 | August 2023 | No model card |
| Grok-1.5 | March 2024 | Blog only (https://x.ai/news/grok-1.5) |
| Grok-1.5V | April 2024 | No model card |
| Grok-2 / 2 mini | August 2024 | Blog only (https://x.ai/news/grok-2) |
| Grok-3 / 3 mini | February 2025 | Blog only (https://x.ai/news/grok-3) |

**Note**: Grok 4 initially launched (July 2025) without a safety report, drawing public criticism. Model card published retroactively in August 2025.

### 3. xAI Risk Management Framework (Draft)

- **Date**: February 20, 2025
- **URL**: https://data.x.ai/2025.02.20-RMF-Draft.pdf
- **Models**: General framework
- **Content**: Dual-use cyber capability eval methodology, references CyBench and WMDP

### 4. xAI Risk Management Framework (Updated)

- **Date**: August 20, 2025
- **URL**: https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf
- **Models**: General framework
- **Content**: Three-category safety eval structure, CBRN and cyber risk management, tiered access

### 5. Grok 4 Model Card

- **Date**: August 20, 2025
- **URL**: https://data.x.ai/2025-08-20-grok-4-model-card.pdf
- **Models**: Grok 4 Web, Grok 4 API
- **Benchmarks**:
  - WMDP-Cyber: **79%**
  - CyBench: **43%** unguided success rate, 40 CTF challenges (UK AISI Inspect framework)
  - AgentHarm (**0.14**), AgentDojo (**0.02**), MASK (0.43), MakeMeSay (**0.12**), Sycophancy (0.07)
  - Internal harmful request datasets (6 languages)
  - UK AISI third-party testing: below human professional in realistic cyber

### 6. Grok 4 Fast Model Card

- **Date**: September 19, 2025
- **URL**: https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf
- **Models**: Grok 4 Fast
- **Benchmarks**:
  - WMDP-Cyber: **81.4%**
  - CyBench: **30%** unguided success rate
  - AgentHarm (0.08/0.10), AgentDojo (0.00/0.03 attack success)
  - MASK (0.47/0.63), MakeMeSay (0.12), Sycophancy (0.10/0.13)

### 7. Grok Code Fast 1 Model Card

- **Date**: August 26, 2025
- **URL**: https://data.x.ai/2025-08-26-grok-code-fast-1-model-card.pdf
- **Models**: Grok Code Fast 1
- **Benchmarks**: AgentHarm, internal harmful request datasets, model-based input filters
- **Note**: Does not include full dual-use suite (CyBench, WMDP)

### 8. Grok 4.1 Model Card

- **Date**: November 17, 2025
- **URL**: https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf
- **Models**: Grok 4.1 Thinking, Grok 4.1 Non-Thinking
- **Benchmarks**:
  - WMDP-Cyber: **84%**, WMDP-Bio: **87%**
  - CyBench: **39%** unguided success rate (substantially below human experts; slight regression from Grok 4's 43%)
  - AgentHarm: **0.14** (T) / **0.04** (NT)
  - AgentDojo: **0.05** (T) / **0.01** (NT), MASK (0.49/0.46), MakeMeSay (0% as attacker), Sycophancy (0.19/0.23)
  - VCT (0.60), BioLP-Bench (0.47), ProtocolQA (0.76), FigQA (0.29), CloningScenarios (0.45)
  - Input filter eval: 0.03 FN biology, 0.00 FN chemistry

### 9. xAI Frontier AI Framework (FAIF)

- **Date**: December 31, 2025
- **URL**: https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf
- **Models**: General framework
- **Content**: TFAIA compliance, WMDP-Cyber references, AI-powered input/output filters

---

## Key Observations

1. **Documentation gap**: Grok-0 through Grok-3 have no cybersecurity benchmarks in published documents
2. **Cyber evals started with Grok 4** (August 2025) — much later than other companies
3. **Consistent framework from Grok 4 onward**: Same three-category structure and benchmark suite
4. **UK AISI third-party validation**: Grok 4 below human professional in realistic cyber
5. **Retroactive publication**: Grok 4 released without safety report; published a month later
6. **All documents hosted at**: data.x.ai, linked from https://x.ai/safety
