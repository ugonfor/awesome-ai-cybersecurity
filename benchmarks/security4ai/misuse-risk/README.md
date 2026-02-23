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
- **Summary**: Agent misuse benchmark measuring completion rate of malicious agentic tasks; LLMs are surprisingly compliant with malicious agent requests without jailbreaking. Lower completion rate is safer. ICLR 2025.
- **Results (Completion Rate, lower is safer)**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 (API) | 0.14 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4 Fast (R/NR) | 0.08 / 0.10 | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 (T/NT) | 0.14 / 0.04 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
- **Notes**: Non-Thinking/Non-Reasoning variants generally show better safety (lower completion rates). Grok 4.1 Non-Thinking achieves the lowest rate (0.04).

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

### Malicious Computer Use Refusal (Anthropic)
- **Category**: Security4AI > Misuse Risk > Refusal > Agentic
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: 112 tasks, extended + standard thinking evaluated
- **Dataset**: Closed
- **Summary**: Measures refusal rate when models are asked to perform malicious actions through computer use (without mitigations). Higher is safer.
- **Results (Refusal Rate, higher is safer)**:
  | Model | Refusal Rate | Date | Source |
  |---|---|---|---|
  | Claude Sonnet 4.6 | 99.38% | 2026.02 | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
  | Claude Opus 4.5 | 88.39% | 2025.11 | [System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
  | Claude Opus 4.6 | 88.34% | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |
  | Claude Sonnet 4.5 | 86.08% | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
  | Claude Haiku 4.5 | 77.68% | 2025.10 | [System Card](https://www.anthropic.com/claude-haiku-4-5-system-card) |
- **Notes**: Claude Sonnet 4.6 achieves the highest refusal rate (99.38%), surpassing all previous models including Opus 4.6 (88.34%).

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
