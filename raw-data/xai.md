# xAI: Cybersecurity Evaluation Documentation

## Overview

- **Total Documents**: 9 (8 PDFs at data.x.ai + 1 Grok-1 model card page; Grok 4.1 Fast blog post tracked but no model card)
- **Date Range**: 2023-11 ~ 2025-12
- **Risk Framework**: Risk Management Framework ([Draft PDF](https://data.x.ai/2025.02.20-RMF-Draft.pdf)) / Frontier AI Framework (FAIF) ([PDF](https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf))
- **Backbone Models**: Grok 4.1, Grok 4.1 Fast, Grok 4, Grok 4 Fast
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

  **Abuse Potential (Table 1):**

  | Benchmark | Category | Score (API) | Score (Web) | Methodology | Source Page/Section |
  |---|---|---|---|---|---|
  | Chat Refusals | Security4AI > Misuse Risk | 0.00 | 0.00 | Answer rate on violative prompts (multilingual) | Table 1 |
  | + User Jailbreak | Security4AI > Model Robustness | 0.00 | 0.01 | Answer rate under user jailbreak | Table 1 |
  | + System Jailbreak | Security4AI > Model Robustness | 0.01 | — | Answer rate under system jailbreak (Web does not accept custom system prompts) | Table 1 |
  | AgentHarm | Security4AI > Misuse Risk | 0.14 | — | Completion rate of malicious agentic tasks | Table 1 |
  | AgentDojo | Security4AI > Model Robustness | 0.02 | — | Prompt injection attack success rate | Table 1 |

  **Concerning Propensities (Table 2):**

  | Benchmark | Category | Score (API) | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | MASK | Security4AI > Alignment | 0.43 | Deception measurement (faithfully reporting beliefs) | Table 2 |
  | Soft Bias (Internal) | Other (Political Bias) | 0.36 | Average bias on paired sociopolitical questions | Table 2 |
  | Sycophancy | Security4AI > Alignment | 0.07 | Ignoring own judgment to agree with misleading user input | Table 2 |

  **Dual-Use Capabilities (Table 3):**

  | Benchmark | Category | Score (API) | Score (Web) | Methodology | Source Page/Section |
  |---|---|---|---|---|---|
  | WMDP-Cyber | AI4Security > Cyber Knowledge | 79% | — | MC questions, cyber killchain (recon, weaponization, exploitation, post-exploitation) | Table 3 |
  | WMDP-Bio | Other (Biology) | 87% | 88% | MC questions, biological weapons knowledge | Table 3 |
  | WMDP-Chem | Other (Chemistry) | 83% | 85% | MC questions, dual-use chemical knowledge | Table 3 |
  | CyBench | AI4Security > Offensive Capability | 43% unguided | — | 40 professional CTF tasks, UK AISI Inspect framework | Table 3 |
  | BioLP-Bench | Other (Biology) | 47% | 44% | Identifying issues in biological lab protocols | Table 3 |
  | VCT | Other (Virology) | 60% | 71% | Expert-level virology troubleshooting (text-only) | Table 3 |
  | MakeMeSay | Security4AI > Alignment | 0.12 | — | Persuasion eval (win rate against non-thinking Grok-3-Mini defender) | Table 3 |

- **Agent Setup**: UK AISI Inspect framework for CyBench evaluation
- **Key Findings**: First xAI model with cybersecurity benchmarks. UK AISI third-party testing confirmed model is below human professional in realistic cyber scenarios. Also evaluated on internal harmful request datasets in 6 languages. Grok 4 API and Web show different scores on biology benchmarks (VCT: 60% API vs 71% Web). Superhuman performance on BioLP-Bench (47% vs 38.4% human) and VCT (60% vs 22.1% human). Chat refusal rates near zero for both API and Web (API: 0.00/0.00/0.01 for standard/user-jailbreak/system-jailbreak; Web: 0.00/0.01/- with system jailbreak not evaluated since Web does not accept custom system prompts). Political bias measured at 0.36 (Soft Bias, internal eval).
- **Notes**: Grok 4 initially launched (July 2025) without a safety report, drawing public criticism. Model card published retroactively in August 2025. CyBench is the same benchmark as [Cybench](https://cybench.github.io/) ([arxiv:2408.08926](https://arxiv.org/abs/2408.08926)); xAI uses alternate capitalization. CyBench and WMDP-Cyber only evaluated for API, not Web.

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

  **Abuse Potential (Table 1):**

  | Benchmark | Category | Score (R) | Score (NR) | Methodology | Source Page/Section |
  |---|---|---|---|---|---|
  | Chat Refusals | Security4AI > Misuse Risk | 0.00 | 0.00 | Answer rate on violative prompts (multilingual) | Table 1 |
  | + User Jailbreak | Security4AI > Model Robustness | 0.00 | 0.00 | Answer rate under user jailbreak | Table 1 |
  | + System Jailbreak | Security4AI > Model Robustness | 0.00 | 0.01 | Answer rate under system jailbreak | Table 1 |
  | AgentHarm | Security4AI > Misuse Risk | 0.08 | 0.10 | Completion rate of malicious agentic tasks | Table 1 |
  | AgentDojo | Security4AI > Model Robustness | 0.00 | 0.03 | Prompt injection attack success rate | Table 1 |

  **Concerning Propensities (Table 2):**

  | Benchmark | Category | Score (R) | Score (NR) | Methodology | Source Page/Section |
  |---|---|---|---|---|---|
  | MASK | Security4AI > Alignment | 0.47 | 0.63 | Deception measurement | Table 2 |
  | Soft Bias (Internal) | Other (Political Bias) | 0.79 | 0.89 | Average bias on paired sociopolitical questions | Table 2 |
  | Sycophancy | Security4AI > Alignment | 0.10 | 0.13 | Ignoring own judgment to agree with misleading input | Table 2 |

  **Dual-Use Capabilities (Table 3):**

  | Benchmark | Category | Score (R) | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | WMDP-Cyber | AI4Security > Cyber Knowledge | 81.4% | MC questions, cyber killchain | Table 3 |
  | WMDP-Bio | Other (Biology) | 85.2% | MC questions, biological weapons knowledge | Table 3 |
  | WMDP-Chem | Other (Chemistry) | 77.5% | MC questions, dual-use chemical knowledge | Table 3 |
  | CyBench | AI4Security > Offensive Capability | 30% unguided | 40 professional CTF tasks, UK AISI Inspect framework | Table 3 |
  | BioLP-Bench | Other (Biology) | 39.0% | Identifying issues in biological lab protocols | Table 3 |
  | VCT | Other (Virology) | 54.5% | Expert-level virology troubleshooting (text-only) | Table 3 |
  | MakeMeSay | Security4AI > Alignment | 0.12 | Persuasion eval (win rate against non-thinking Grok-3-Mini defender) | Table 3 |

  R = Reasoning mode, NR = Non-Reasoning mode. Dual-use benchmarks (Table 3) reported with reasoning enabled only.

- **Agent Setup**: UK AISI Inspect framework for CyBench evaluation
- **Key Findings**: Higher WMDP-Cyber score (81.4%) than Grok 4 (79%) but lower CyBench performance (30% vs 43%), suggesting knowledge gains did not translate to practical CTF capability. Lower AgentHarm scores indicate better safety behavior. Non-reasoning mode increases dishonesty rate substantially (0.63 vs 0.47). WMDP-Bio at 85.2%, lower than Grok 4's 87%. Dual-use capabilities remain below Grok 4 overall. Chat refusal rates near zero across both modes. Political bias notably high (Soft Bias: R=0.79, NR=0.89) compared to Grok 4 API (0.36).

### 8. Grok 4.1 Model Card

- **Date**: 2025-11-17
- **URL**: https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf
- **Models**: Grok 4.1 Thinking, Grok 4.1 Non-Thinking
- **Type**: Model Card
- **Cyber Risk Level**: Substantially below human experts on CyBench
- **Benchmarks Reported**:

  **Abuse Potential (Table 1):**

  | Benchmark | Category | Score (T) | Score (NT) | Methodology | Source |
  |---|---|---|---|---|---|
  | Chat Refusals | Security4AI > Misuse Risk | 0.07 | 0.05 | Answer rate on violative prompts (multilingual) | Table 1 |
  | + User Jailbreak | Security4AI > Model Robustness | 0.02 | 0.00 | Answer rate under user jailbreak | Table 1 |
  | + System Jailbreak | Security4AI > Model Robustness | 0.02 | 0.00 | Answer rate under system jailbreak | Table 1 |
  | AgentHarm | Security4AI > Misuse Risk | 0.14 | 0.04 | Completion rate of malicious agentic tasks | Table 1 |
  | AgentDojo | Security4AI > Model Robustness | 0.05 | 0.01 | Prompt injection attack success rate | Table 1 |

  **Input Filter (Table 2):**

  | Evaluation | Metric | Score | Score (+ Prompt Injection) | Source |
  |---|---|---|---|---|
  | Restricted Biology | false negative rate | 0.03 | 0.20 | Table 2 |
  | Restricted Chemistry | false negative rate | 0.00 | 0.12 | Table 2 |

  **Concerning Propensities (Table 3) -- cross-model comparison:**

  | Benchmark | Category | Grok 4 | Grok 4.1 T | Grok 4.1 NT | Source |
  |---|---|---|---|---|---|
  | MASK | Security4AI > Alignment | 0.43 | 0.49 | 0.46 | Table 3 |
  | Sycophancy | Security4AI > Alignment | 0.07 | 0.19 | 0.23 | Table 3 |

  **Dual-Use Capabilities (Table 4) -- cross-model comparison with human baselines:**

  | Benchmark | Category | Grok 4 | Grok 4.1 T | Human Baseline | Source |
  |---|---|---|---|---|---|
  | WMDP-Cyber | AI4Security > Cyber Knowledge | 79% | 84% | — | Table 4 |
  | WMDP-Bio | Other (Biology) | 87% | 87% | 61% | Table 4 |
  | WMDP-Chem | Other (Chemistry) | 83% | 84% | 43% | Table 4 |
  | CyBench | AI4Security > Offensive Capability | 43% | 39% | — | Table 4 |
  | VCT | Other (Virology) | 60% | 61% | 22% | Table 4 |
  | BioLP-Bench | Other (Biology) | 47% | 37% | 38% | Table 4 |
  | ProtocolQA | Other (Biology) | 76% | 79% | 79% | Table 4 |
  | FigQA | Other (Biology) | 29% | 34% | 77% | Table 4 |
  | CloningScenarios | Other (Biology) | 45% | 46% | 60% | Table 4 |
  | MakeMeSay | Security4AI > Alignment | 13% | 0% | — | Table 4 |

  T = Thinking mode, NT = Non-Thinking mode. Dual-use benchmarks (Table 4) reported for Thinking mode only with safeguards removed.

- **Agent Setup**: UK AISI Inspect framework for CyBench evaluation
- **Key Findings**: Highest WMDP-Cyber score in xAI lineup (84%), but CyBench regressed slightly from Grok 4 (39% vs 43%). 87% WMDP score is WMDP-Bio, NOT WMDP-Cyber. Non-Thinking variant shows better safety on AgentHarm (0.04 vs 0.14). MakeMeSay score of 0% as attacker indicates inability to manipulate defenders (down from Grok 4's 13%). Expanded CBRN evaluation suite beyond previous models. Sycophancy and MASK dishonesty both increased from Grok 4 (0.07->0.19 sycophancy, 0.43->0.49 MASK). Input filter FN rate increases under prompt injection attack (bio: 0.03->0.20, chem: 0.00->0.12).
- **Cross-Model Comparison Notes**: Table 4 shows Grok 4 MakeMeSay as 0.13 (vs 0.12 in Grok 4's own card); this minor discrepancy may reflect evaluation variance. Table 3 provides the first official cross-model comparison of alignment metrics across Grok versions. Table 4 includes human expert baselines from published literature.
- **Methodology Note**: The Grok 4.1 model card acknowledges that "results in previous model cards were reported with an error in the evaluation settings, where only the English prompts were evaluated." Grok 4.1 reports true multilingual refusal results, which are **not directly comparable** to previous model card refusal scores.
- **Notes**: WMDP-Bio 87% must not be conflated with WMDP-Cyber 84%. MASK benchmark created by CAIS ([arxiv:2503.03750](https://arxiv.org/abs/2503.03750)), not UC Berkeley. MakeMeSay created by OpenAI / Google DeepMind ([arxiv:2412.16720](https://arxiv.org/abs/2412.16720)). AgentHarm created by EPFL, Gray Swan, UK AISI, Oxford, CMU. MakeMeSay measured as win rate against non-thinking Grok-3-Mini defender.

### 9. Grok 4.1 Fast (No Model Card Yet)

- **Date**: 2025-11-20 (announced)
- **URL**: https://x.ai/news/grok-4-1-fast (blog post only)
- **Models**: Grok 4.1 Fast (reasoning and non-reasoning modes)
- **Type**: Blog announcement (no model card published as of 2026-02-23)
- **Cyber Risk Level**: Not evaluated in public documentation
- **Benchmarks Reported**: None in official safety documentation
- **Agent Setup**: N/A
- **Key Findings**: Grok 4.1 Fast was announced three days after the Grok 4.1 model card but has no separate model card or safety report. The blog post focuses on general capabilities (2M token context, agent tools API) without safety benchmark scores. This represents a documentation gap similar to the initial Grok 4 launch without a safety report.
- **Notes**: Despite being listed as a backbone model, no cybersecurity benchmark data is publicly available for Grok 4.1 Fast. Third-party reviews note roughly half the hallucination rate of Grok 4 Fast but do not include safety benchmark scores.

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
| Grok 4.1 Fast | 2025-11-20 | Blog only, no model card | https://x.ai/news/grok-4-1-fast |

**Note**: Cybersecurity evaluations began with Grok 4 (August 2025), significantly later than other AI companies. Models from Grok-0 through Grok-3 have no published cybersecurity benchmark results. Grok 4.1 Fast (Nov 2025) also lacks a model card as of Feb 2026.

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
| 2025-11-17 | Grok 4.1 Model Card (WMDP-Cyber 84%, CyBench 39%; expanded CBRN suite; first cross-model comparison table) |
| 2025-11-20 | Grok 4.1 Fast announced (no model card; blog only at https://x.ai/news/grok-4-1-fast) |
| 2025-12-31 | Frontier AI Framework (FAIF) published (TFAIA compliance) |

---

## Summary of Cyber Benchmark Scores

### Primary Cyber Benchmarks

| Model | Date | WMDP-Cyber | CyBench (unguided) | AgentHarm | AgentDojo | MASK | MakeMeSay | Sycophancy |
|---|---|---|---|---|---|---|---|---|
| Grok 4 (API) | 2025-08 | 79% | 43% | 0.14 | 0.02 | 0.43 | 0.12 | 0.07 |
| Grok 4 Fast (R/NR) | 2025-09 | 81.4% | 30% | 0.08/0.10 | 0.00/0.03 | 0.47/0.63 | 0.12 | 0.10/0.13 |
| Grok 4.1 (T/NT) | 2025-11 | 84% | 39% | 0.14/0.04 | 0.05/0.01 | 0.49/0.46 | 0% | 0.19/0.23 |
| Grok 4.1 Fast | 2025-11 | — | — | — | — | — | — | — |

R = Reasoning, NR = Non-Reasoning, T = Thinking, NT = Non-Thinking. WMDP-Cyber and CyBench reported with reasoning/thinking enabled only. Grok 4.1 Fast has no model card yet.

### Chat Refusals & Adversarial Robustness (from model cards)

| Model | Refusals | + User Jailbreak | + System Jailbreak | Source |
|---|---|---|---|---|
| Grok 4 (API) | 0.00 | 0.00 | 0.01 | Grok 4 Card Table 1 |
| Grok 4 (Web) | 0.00 | 0.01 | — | Grok 4 Card Table 1 |
| Grok 4 Fast (R/NR) | 0.00/0.00 | 0.00/0.00 | 0.00/0.01 | Grok 4 Fast Card Table 1 |
| Grok 4.1 (T/NT) | 0.07/0.05 | 0.02/0.00 | 0.02/0.00 | Grok 4.1 Card Table 1 |

Note: Grok 4.1 card acknowledges previous model cards had an evaluation error (English-only prompts). Grok 4.1 reports true multilingual refusal results, making refusal scores not directly comparable across model generations.

### Political Bias (Soft Bias, Internal Eval)

| Model | Soft Bias (R/default) | Soft Bias (NR) | Source |
|---|---|---|---|
| Grok 4 (API) | 0.36 | — | Grok 4 Card Table 2 |
| Grok 4 Fast (R/NR) | 0.79 | 0.89 | Grok 4 Fast Card Table 2 |

### Extended Dual-Use Benchmarks (from model cards)

| Model | WMDP-Bio | WMDP-Chem | VCT | BioLP-Bench | ProtocolQA | FigQA | CloningScenarios |
|---|---|---|---|---|---|---|---|
| Grok 4 (API) | 87% | 83% | 60% | 47% | 76%* | 29%* | 45%* |
| Grok 4 (Web) | 88% | 85% | 71% | 44% | — | — | — |
| Grok 4 Fast | 85.2% | 77.5% | 54.5% | 39.0% | — | — | — |
| Grok 4.1 T | 87% | 84% | 61% | 37% | 79% | 34% | 46% |
| Human Baseline | 61% | 43% | 22% | 38% | 79% | 77% | 60% |

\* Grok 4 ProtocolQA, FigQA, CloningScenarios values sourced from Grok 4.1 Model Card Table 4 cross-model comparison (not present in Grok 4's own model card Table 3).

### Cross-Model Comparison (from Grok 4.1 Model Card Table 4)

The Grok 4.1 model card is the first xAI document to provide a side-by-side comparison of Grok 4 and Grok 4.1 scores in the same table (Table 4), along with human expert baselines. Key deltas:

| Benchmark | Grok 4 | Grok 4.1 T | Delta | Direction |
|---|---|---|---|---|
| WMDP-Cyber | 79% | 84% | +5 | Better knowledge |
| CyBench | 43% | 39% | -4 | Worse practical CTF |
| MakeMeSay | 13% | 0% | -13 | Better safety (lower = safer) |
| MASK | 0.43 | 0.49 | +0.06 | Worse honesty (higher = more deceptive) |
| Sycophancy | 0.07 | 0.19 | +0.12 | Worse sycophancy |

Note: Grok 4 MakeMeSay reported as 0.12 in its own card but 0.13 in the Grok 4.1 card comparison column. Minor evaluation variance.

**Key Observations**:
1. **Documentation gap**: Grok-0 through Grok-3 have no cybersecurity benchmarks in published documents
2. **Grok 4.1 Fast documentation gap**: Released Nov 2025, no model card as of Feb 2026
3. **Cyber evals started with Grok 4** (August 2025) — much later than other companies
4. **Consistent framework from Grok 4 onward**: Same three-category structure and benchmark suite
5. **UK AISI third-party validation**: Grok 4 assessed as below human professional in realistic cyber
6. **Retroactive publication**: Grok 4 released without safety report; published a month later
7. **WMDP-Cyber trending up** (79% -> 81.4% -> 84%) but **CyBench inconsistent** (43% -> 30% -> 39%)
8. **Safety tradeoff in Grok 4.1**: Better on MakeMeSay (0% vs 12-13%) but worse on sycophancy (0.19 vs 0.07) and MASK dishonesty (0.49 vs 0.43) compared to Grok 4
9. **Evaluation methodology change**: Grok 4.1 card acknowledges previous model cards had an evaluation error (English-only prompts); Grok 4.1 uses true multilingual refusal eval, making refusal scores not directly comparable to Grok 4/4 Fast
10. **Input filter vulnerability**: Restricted bio/chem filters show increased FN under prompt injection (bio: 0.03 -> 0.20, chem: 0.00 -> 0.12)
11. **All documents hosted at**: data.x.ai, linked from https://x.ai/safety
