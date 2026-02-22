# xAI: Cybersecurity Evaluation Documentation

## Overview

- **Total Documents**: 9
- **Date Range**: 2023-11 ~ 2025-12
- **Risk Framework**: Risk Management Framework ([Draft PDF](https://data.x.ai/2025.02.20-RMF-Draft.pdf)) / Frontier AI Framework (FAIF) ([PDF](https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf))
- **Backbone Models**: Grok 4.1, Grok 4 Fast
- **Primary Benchmarks**: WMDP-Cyber, CyBench (=Cybench), AgentHarm, AgentDojo, MASK, MakeMeSay, Sycophancy
- **All Documents Hosted At**: data.x.ai, linked from https://x.ai/safety

---

## Frameworks

### 1. xAI Risk Management Framework (Draft)

- **Date**: 2025-02-20
- **URL**: https://data.x.ai/2025.02.20-RMF-Draft.pdf
- **Models**: General framework (no model-specific evaluations)
- **Type**: Framework
- **Cyber Risk Level**: N/A (framework document)
- **Benchmarks Reported**: None (defines methodology)
- **Agent Setup**: N/A
- **Key Findings**: Establishes dual-use cyber capability evaluation methodology; references CyBench and WMDP as primary cyber benchmarks. Three evaluation categories: abuse potential, concerning propensities, and dual-use capabilities.

### 2. xAI Risk Management Framework (Updated)

- **Date**: 2025-08-20
- **URL**: https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf
- **Models**: General framework (no model-specific evaluations)
- **Type**: Framework
- **Cyber Risk Level**: N/A (framework document)
- **Benchmarks Reported**: None (defines methodology)
- **Agent Setup**: N/A
- **Key Findings**: Updates the three-category safety evaluation structure. Covers CBRN and cyber risk management with tiered access controls. Published same day as Grok 4 Model Card.

### 3. xAI Frontier AI Framework (FAIF)

- **Date**: 2025-12-31
- **URL**: https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf
- **Models**: General framework (no model-specific evaluations)
- **Type**: Framework
- **Cyber Risk Level**: N/A (framework document)
- **Benchmarks Reported**: None (references WMDP-Cyber as part of evaluation suite)
- **Agent Setup**: N/A
- **Key Findings**: TFAIA compliance document. References AI-powered input/output filters for safety. Continues to use WMDP-Cyber as a core cyber benchmark.

---

## Model Evaluations

### 4. Grok-1 Model Card

- **Date**: 2023-11
- **URL**: https://x.ai/news/grok/model-card
- **Models**: Grok-1 (314B MoE)
- **Type**: Model Card
- **Cyber Risk Level**: N/A (no cybersecurity evaluations)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | GSM8k | General | — | Math reasoning | Model Card |
  | MMLU | General | 73% | Multiple choice | Model Card |
  | HumanEval | General | 63.2% | Code generation | Model Card |
  | MATH | General | — | Math reasoning | Model Card |

- **Agent Setup**: N/A
- **Key Findings**: First xAI model card. No cybersecurity-specific benchmarks included; only general capability evaluations.

### 5. Grok 4 Model Card

- **Date**: 2025-08-20
- **URL**: https://data.x.ai/2025-08-20-grok-4-model-card.pdf
- **Models**: Grok 4 Web, Grok 4 API
- **Type**: Model Card
- **Cyber Risk Level**: Below human professional in realistic cyber (UK AISI assessment)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | WMDP-Cyber | AI4Security > Cyber Knowledge | 79% | MC questions, cyber killchain (recon, weaponization, exploitation, post-exploitation) | Model Card |
  | CyBench | AI4Security > Offensive Capability | 43% unguided | 40 professional CTF tasks, UK AISI Inspect framework | Model Card |
  | AgentHarm | Security4AI > Misuse Risk | 0.14 | Completion rate of malicious agentic tasks | Model Card |
  | AgentDojo | Security4AI > Model Robustness | 0.02 | Prompt injection robustness in agentic settings | Model Card |
  | MASK | Security4AI > Alignment | 0.43 | Deception measurement (faithfully reporting beliefs) | Model Card |
  | MakeMeSay | Security4AI > Alignment | 0.12 | Persuasion eval (manipulating defender into saying codeword) | Model Card |
  | Sycophancy | Security4AI > Alignment | 0.07 | Ignoring own judgment to agree with misleading user input | Model Card |

- **Agent Setup**: UK AISI Inspect framework for CyBench evaluation
- **Key Findings**: First xAI model with cybersecurity benchmarks. UK AISI third-party testing confirmed model is below human professional in realistic cyber scenarios. Also evaluated on internal harmful request datasets in 6 languages.
- **Notes**: Grok 4 initially launched (July 2025) without a safety report, drawing public criticism. Model card published retroactively in August 2025. CyBench is the same benchmark as [Cybench](https://cybench.github.io/) ([arxiv:2408.08926](https://arxiv.org/abs/2408.08926)); xAI uses alternate capitalization.

### 6. Grok Code Fast 1 Model Card

- **Date**: 2025-08-26
- **URL**: https://data.x.ai/2025-08-26-grok-code-fast-1-model-card.pdf
- **Models**: Grok Code Fast 1
- **Type**: Model Card
- **Cyber Risk Level**: Not explicitly stated
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | AgentHarm | Security4AI > Misuse Risk | Reported (score not public) | Completion rate of malicious agentic tasks | Model Card |
  | Internal harmful request datasets | Security4AI > Misuse Risk | Reported | Model-based input filters | Model Card |

- **Agent Setup**: N/A
- **Key Findings**: Code-specialized model. Does not include full dual-use evaluation suite (no CyBench, no WMDP). Evaluated primarily on misuse/safety metrics rather than offensive capability benchmarks.

### 7. Grok 4 Fast Model Card

- **Date**: 2025-09-19
- **URL**: https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf
- **Models**: Grok 4 Fast
- **Type**: Model Card
- **Cyber Risk Level**: Not explicitly stated (consistent with Grok 4 assessment)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | WMDP-Cyber | AI4Security > Cyber Knowledge | 81.4% | MC questions, cyber killchain | Model Card |
  | CyBench | AI4Security > Offensive Capability | 30% unguided | 40 professional CTF tasks, UK AISI Inspect framework | Model Card |
  | AgentHarm | Security4AI > Misuse Risk | 0.08 / 0.10 | Completion rate of malicious agentic tasks | Model Card |
  | AgentDojo | Security4AI > Model Robustness | 0.00 / 0.03 | Prompt injection attack success rate | Model Card |
  | MASK | Security4AI > Alignment | 0.47 / 0.63 | Deception measurement | Model Card |
  | MakeMeSay | Security4AI > Alignment | 0.12 | Persuasion eval | Model Card |
  | Sycophancy | Security4AI > Alignment | 0.10 / 0.13 | Ignoring own judgment to agree with misleading input | Model Card |

- **Agent Setup**: UK AISI Inspect framework for CyBench evaluation
- **Key Findings**: Higher WMDP-Cyber score (81.4%) than Grok 4 (79%) but lower CyBench performance (30% vs 43%), suggesting knowledge gains did not translate to practical CTF capability. Lower AgentHarm scores indicate better safety behavior.

### 8. Grok 4.1 Model Card

- **Date**: 2025-11-17
- **URL**: https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf
- **Models**: Grok 4.1 Thinking, Grok 4.1 Non-Thinking
- **Type**: Model Card
- **Cyber Risk Level**: Substantially below human experts on CyBench
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | WMDP-Cyber | AI4Security > Cyber Knowledge | 84% | MC questions, cyber killchain | Model Card |
  | WMDP-Bio | Other (Biology) | 87% | MC questions, biological weapons knowledge | Model Card |
  | CyBench | AI4Security > Offensive Capability | 39% unguided | 40 professional CTF tasks, UK AISI Inspect framework | Model Card |
  | AgentHarm | Security4AI > Misuse Risk | 0.14 (T) / 0.04 (NT) | Completion rate of malicious agentic tasks; T=Thinking, NT=Non-Thinking | Model Card |
  | AgentDojo | Security4AI > Model Robustness | 0.05 (T) / 0.01 (NT) | Prompt injection attack success rate | Model Card |
  | MASK | Security4AI > Alignment | 0.49 / 0.46 | Deception measurement (CAIS, [arxiv:2503.03750](https://arxiv.org/abs/2503.03750)) | Model Card |
  | MakeMeSay | Security4AI > Alignment | 0% as attacker | Persuasion eval (OpenAI / Google DeepMind) | Model Card |
  | Sycophancy | Security4AI > Alignment | 0.19 / 0.23 | Ignoring own judgment to agree with misleading input | Model Card |
  | VCT | Other (Virology) | 0.60 | Virology capability test | Model Card |
  | BioLP-Bench | Other (Biology) | 0.47 | Biological lab protocol benchmark | Model Card |
  | ProtocolQA | Other (Biology) | 0.76 | Protocol question answering | Model Card |
  | FigQA | Other (Biology) | 0.29 | Figure-based question answering | Model Card |
  | CloningScenarios | Other (Biology) | 0.45 | Cloning scenario evaluation | Model Card |
  | Input Filter (Biology) | Security4AI > Misuse Risk | 0.03 FN | False negative rate for biology-related harmful requests | Model Card |
  | Input Filter (Chemistry) | Security4AI > Misuse Risk | 0.00 FN | False negative rate for chemistry-related harmful requests | Model Card |

- **Agent Setup**: UK AISI Inspect framework for CyBench evaluation
- **Key Findings**: Highest WMDP-Cyber score in xAI lineup (84%), but CyBench regressed slightly from Grok 4 (39% vs 43%). 87% WMDP score is WMDP-Bio, NOT WMDP-Cyber. Non-Thinking variant shows better safety on AgentHarm (0.04 vs 0.14). MakeMeSay score of 0% as attacker indicates inability to manipulate defenders. Expanded CBRN evaluation suite beyond previous models.
- **Notes**: WMDP-Bio 87% must not be conflated with WMDP-Cyber 84%. MASK benchmark created by CAIS ([arxiv:2503.03750](https://arxiv.org/abs/2503.03750)), not UC Berkeley. MakeMeSay created by OpenAI / Google DeepMind. AgentHarm created by EPFL, Gray Swan, UK AISI, Oxford, CMU.

---

## Models Without Cyber Evals

| Model | Release Date | Status | Notes |
|---|---|---|---|
| Grok-0 | 2023-08 | No model card | Prototype; no public documentation |
| Grok-1 | 2023-11 | Model card, no cyber evals | General benchmarks only (MMLU 73%, HumanEval 63.2%) |
| Grok-1.5 | 2024-03 | Blog only | https://x.ai/news/grok-1.5 |
| Grok-1.5V | 2024-04 | No model card | Vision model; no public documentation |
| Grok-2 / 2 mini | 2024-08 | Blog only | https://x.ai/news/grok-2 |
| Grok-3 / 3 mini | 2025-02 | Blog only | https://x.ai/news/grok-3 |

**Note**: Cybersecurity evaluations began with Grok 4 (August 2025), significantly later than other AI companies. Models from Grok-0 through Grok-3 have no published cybersecurity benchmark results.

---

## Key Milestones

| Date | Event |
|---|---|
| 2023-11 | Grok-1 Model Card published (no cyber evals) |
| 2025-02-20 | Risk Management Framework Draft released |
| 2025-07 | Grok 4 launched without safety report (drew criticism) |
| 2025-08-20 | Grok 4 Model Card + Updated RMF published retroactively; first cyber evals (WMDP-Cyber 79%, CyBench 43%) |
| 2025-08-26 | Grok Code Fast 1 Model Card (limited safety evals) |
| 2025-09-19 | Grok 4 Fast Model Card (WMDP-Cyber 81.4%, CyBench 30%) |
| 2025-11-17 | Grok 4.1 Model Card (WMDP-Cyber 84%, CyBench 39%; expanded CBRN suite) |
| 2025-12-31 | Frontier AI Framework (FAIF) published (TFAIA compliance) |

---

## Summary of Cyber Benchmark Scores

| Model | Date | WMDP-Cyber | CyBench (unguided) | AgentHarm | AgentDojo | MASK | MakeMeSay | Sycophancy |
|---|---|---|---|---|---|---|---|---|
| Grok 4 | 2025-08 | 79% | 43% | 0.14 | 0.02 | 0.43 | 0.12 | 0.07 |
| Grok 4 Fast | 2025-09 | 81.4% | 30% | 0.08/0.10 | 0.00/0.03 | 0.47/0.63 | 0.12 | 0.10/0.13 |
| Grok 4.1 (T/NT) | 2025-11 | 84% | 39% | 0.14/0.04 | 0.05/0.01 | 0.49/0.46 | 0% | 0.19/0.23 |

**Key Observations**:
1. **Documentation gap**: Grok-0 through Grok-3 have no cybersecurity benchmarks in published documents
2. **Cyber evals started with Grok 4** (August 2025) — much later than other companies
3. **Consistent framework from Grok 4 onward**: Same three-category structure and benchmark suite
4. **UK AISI third-party validation**: Grok 4 assessed as below human professional in realistic cyber
5. **Retroactive publication**: Grok 4 released without safety report; published a month later
6. **WMDP-Cyber trending up** (79% -> 81.4% -> 84%) but **CyBench inconsistent** (43% -> 30% -> 39%)
7. **All documents hosted at**: data.x.ai, linked from https://x.ai/safety
