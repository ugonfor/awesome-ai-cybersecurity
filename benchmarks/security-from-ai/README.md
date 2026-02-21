# Security FROM AI Benchmarks

> Assessing risks posed by AI: misuse potential, dual-use capabilities, deceptive behavior, alignment risks.

---

## Misuse Risk / Dual-use

### [AgentHarm](https://arxiv.org/abs/2410.09024)
- **Category**: Security FROM AI > Misuse > Agentic
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
- **Category**: Security FROM AI > Misuse > Malware
- **Created by**: OpenAI
- **Used by**: OpenAI
- **Scale**: Synthetic, large-scale, dual-use prompts
- **Dataset**: Closed
- **Summary**: Evaluates model capability to generate malware-related content including code generation for malicious purposes.

---

### Harmful Request Refusal
- **Category**: Security FROM AI > Misuse > Refusal
- **Created by**: Multiple (each company's internal version)
- **Used by**: OpenAI, Anthropic, Google, xAI
- **Scale**: Varies (xAI: 6 languages; OpenAI: 97% refusal)
- **Dataset**: Closed
- **Summary**: Measures refusal rate on violative/harmful prompts across categories including cyber exploitation, weapon creation, and social engineering.

---

### Zero-day Discovery Evaluation
- **Category**: Security FROM AI > Dual-use > Vulnerability Discovery
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: Open-source software auditing
- **Dataset**: Closed
- **Summary**: Evaluates whether models can autonomously discover novel, previously unknown vulnerabilities — a dual-use capability with both defensive value and offensive risk.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude Opus 4.6 | 500+ novel vulnerabilities | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

---

## Behavioral / Alignment

### [MASK](https://arxiv.org/abs/2503.03750)
- **Category**: Security FROM AI > Behavioral > Deception
- **Created by**: Center for AI Safety (CAIS)
- **Used by**: xAI
- **Scale**: Multi-scenario deception measurement
- **Dataset**: Open ([GitHub](https://github.com/centerforaisafety/mask))
- **Reference**: [The MASK Benchmark: Disentangling Honesty From Accuracy in AI Systems](https://arxiv.org/abs/2503.03750)
- **Summary**: Measures whether models faithfully report their beliefs or engage in deceptive behavior under pressure.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 0.43 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4.1 Thinking | 0.49 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### MakeMeSay
- **Category**: Security FROM AI > Behavioral > Persuasion
- **Created by**: OpenAI (adapted from Google DeepMind methodology)
- **Used by**: xAI
- **Scale**: Attacker-defender persuasion game
- **Dataset**: Open
- **Summary**: Evaluates model's ability to manipulate another model into saying a specific codeword through persuasion.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4.1 | 0% (as attacker) | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### Sycophancy Evaluation
- **Category**: Security FROM AI > Behavioral > Sycophancy
- **Created by**: Various
- **Used by**: xAI
- **Scale**: User agreement measurement
- **Dataset**: Open
- **Summary**: Measures tendency to abandon correct judgments to agree with misleading user input.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 0.07 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4.1 Thinking | 0.19 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### [Stealth Evaluation](https://arxiv.org/abs/2505.01420)
- **Category**: Security FROM AI > Behavioral > Oversight Evasion
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 5 stealth evaluations
- **Dataset**: Open
- **Reference**: [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Summary**: Tests model's ability to circumvent oversight mechanisms and operate covertly.

---

### [Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Category**: Security FROM AI > Behavioral > Self-Reasoning
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 11 situational awareness evaluations
- **Dataset**: Open
- **Reference**: [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Summary**: Evaluates model's ability to reason about itself and its environment, a prerequisite for autonomous action.

---

### [Sabotage Risk Assessment](https://alignment.anthropic.com/2025/sabotage-risk-report/)
- **Category**: Security FROM AI > Behavioral > Sabotage
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: 9 sabotage pathways
- **Dataset**: Closed
- **Reference**: [Pilot Sabotage Risk Report](https://alignment.anthropic.com/2025/sabotage-risk-report/2025_pilot_risk_report.pdf)
- **Summary**: Evaluates 9 pathways through which AI models could deliberately sabotage their operators. Reviewed by METR.

---

## Academic Benchmarks (Community-Driven)

> The following benchmarks originate from the academic community and are not primarily used in the four major vendors' official model evaluations.

---

*AgentHarm is listed in the vendor section above.*

### [CyberSecEval (Purple Llama) — Misuse Risk Components](https://github.com/meta-llama/PurpleLlama)
- **Category**: Security FROM AI > Misuse > Code Generation / Cyberattack Compliance
- **Created by**: Meta AI
- **Used by**: Meta (Llama evaluations)
- **Scale**: Insecure code generation (50 CWEs, 189 rules); cyberattack compliance (MITRE ATT&CK ontology); 52% average compliance rate across models
- **Dataset**: Open
- **Reference**: [Purple Llama CyberSecEval: A Secure Coding Benchmark for Language Models](https://arxiv.org/abs/2312.04724)
- **Summary**: Measures LLM propensity to generate insecure code and comply with cyberattack requests; found models complied with 52% of attack-assistance requests on average. Part of Meta's Purple Llama safety suite.

---

### [WMDP (Weapons of Mass Destruction Proxy)](https://github.com/centerforaisafety/wmdp)
- **Category**: Security FROM AI > Dual-use > Hazardous Knowledge
- **Created by**: Center for AI Safety (CAIS), Scale AI, 20+ academic institutions
- **Used by**: xAI (WMDP-Cyber subset)
- **Scale**: 3,668 multiple-choice questions across biosecurity, cybersecurity, and chemical security
- **Dataset**: Open (filtered to remove sensitive info)
- **Reference**: [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/abs/2403.03218)
- **Summary**: Measures hazardous knowledge that could enable malicious use in bio/cyber/chem domains; also benchmarks unlearning methods (RMU) for removing hazardous knowledge while retaining general capabilities. ICML 2024.
