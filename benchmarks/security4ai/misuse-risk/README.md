# Security4AI — Misuse Risk Benchmarks

> Preventing harmful use of AI: malicious task completion, harmful content generation, dual-use capability assessment.

---

### [AgentHarm](https://arxiv.org/abs/2410.09024)
- **Category**: Security4AI > Misuse Risk > Agentic
- **Created by**: EPFL, Gray Swan AI, UK AI Safety Institute, University of Oxford, CMU
- **Used by**: xAI
- **Scale**: 110 malicious agent tasks (440 with augmentations) across 11 harm categories
- **Dataset**: Open ([HuggingFace](https://huggingface.co/datasets/ai-safety-institute/AgentHarm))
- **Reference**: [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024)
- **Summary**: Agent misuse benchmark; LLMs are surprisingly compliant with malicious agent requests without jailbreaking. ICLR 2025.
- **Results**:
  | Model | Completion Rate | Date | Source |
  |---|---|---|---|
  | Grok 4 Fast | 8-10% | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 | <14% | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### Malware Benchmark (OpenAI)
- **Category**: Security4AI > Misuse Risk > Malware
- **Created by**: OpenAI
- **Used by**: OpenAI
- **Scale**: Synthetic, large-scale, dual-use prompts
- **Dataset**: Closed
- **Summary**: Evaluates model capability to generate malware-related content including code generation for malicious purposes.

---

### Harmful Request Refusal
- **Category**: Security4AI > Misuse Risk > Refusal
- **Created by**: Multiple (each company's internal version)
- **Used by**: OpenAI, Anthropic, Google, xAI
- **Scale**: Varies (xAI: 6 languages; OpenAI: 97% refusal)
- **Dataset**: Closed
- **Summary**: Measures refusal rate on violative/harmful prompts across categories including cyber exploitation, weapon creation, and social engineering.

---

### Zero-day Discovery Evaluation
- **Category**: Security4AI > Misuse Risk > Dual-use Vulnerability Discovery
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: Open-source software auditing
- **Dataset**: Closed
- **Summary**: Evaluates whether models can autonomously discover novel, previously unknown vulnerabilities — a dual-use capability with both defensive value and offensive risk.
- **Cross-reference**: Also listed under [AI4Security > Offensive Capability](../../ai4security/offensive/README.md) as a capability benchmark.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude Opus 4.6 | 500+ novel vulnerabilities | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

---

## Academic Benchmarks (Community-Driven)

---

### [CyberSecEval (Purple Llama) — Misuse Risk Components](https://github.com/meta-llama/PurpleLlama)
- **Category**: Security4AI > Misuse Risk > Code Generation / Cyberattack Compliance
- **Created by**: Meta AI
- **Used by**: Meta (Llama evaluations)
- **Scale**: Insecure code generation (50 CWEs, 189 rules); cyberattack compliance (MITRE ATT&CK ontology); 52% average compliance rate across models
- **Dataset**: Open
- **Reference**: [Purple Llama CyberSecEval: A Secure Coding Benchmark for Language Models](https://arxiv.org/abs/2312.04724)
- **Summary**: Measures LLM propensity to generate insecure code and comply with cyberattack requests; found models complied with 52% of attack-assistance requests on average. Part of Meta's Purple Llama safety suite.
