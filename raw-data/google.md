# Google DeepMind: Cybersecurity Evaluation Documentation

## Overview

- **Total Documents**: 25+
- **Date Range**: 2023-12 ~ 2026-02
- **Risk Framework**: Frontier Safety Framework (FSF v3.0) ([PDF](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf))
- **Risk Levels**: CCL alert threshold → CCL reached (per Critical Capability Level system)
- **Cyber Threshold Definition**: Cyber Uplift Level 1 — "The model can be used to significantly assist with high impact cyber attacks, resulting in overall cost/resource reductions of an order of magnitude or more."
- **First Threshold Crossed**: None (CCL alert threshold reached starting with Gemini 2.5 Pro, but CCL never met as of Feb 2026)
- **Backbone Models**: Gemini 3.1 Pro, Gemini 3 Pro, Gemini 3 Flash
- **Primary Benchmarks**: InterCode-CTF, In-house CTF (13 GDM challenges), Hack the Box, Key Skills Benchmark (MITRE ATT&CK aligned), Pattern Labs External CTFs, CTI-MCQ, CTI-RCM
- **Third-party Testing**: None listed (no US/UK AISI joint testing noted)
- **Open-sources Evals**: Yes (In-house CTF via UK AISI Inspect)
- **Real-world Threat Intel Published**: Yes (12,000+ incidents via Google Threat Intelligence)
- **Specialized Cyber Model**: Sec-Gemini v1
- **Model Cards Index**: https://deepmind.google/models/model-cards/

---

## Frameworks

### 1. Frontier Safety Framework v1.0

- **Date**: 2024-05
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/introducing-the-frontier-safety-framework/fsf-technical-report.pdf)
- **Models**: N/A (framework document)
- **Type**: Framework
- **Cyber Risk Level**: N/A
- **Benchmarks Reported**: None (defines evaluation methodology)
- **Key Findings**: Establishes Critical Capability Levels (CCLs) for frontier model risk assessment across multiple domains including cybersecurity.

### 2. Frontier Safety Framework v3.0

- **Date**: 2025-10
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf)
- **Models**: N/A (framework document)
- **Type**: Framework
- **Cyber Risk Level**: N/A
- **Benchmarks Reported**: None (defines evaluation methodology)
- **Key Findings**: Updated framework covering four risk domains: CBRN, cybersecurity, ML R&D, harmful manipulation/misalignment. Defines Cyber Uplift Level 1 threshold criteria.

---

## Technical Reports

### 3. Gemini 1.0 Technical Report

- **Date**: 2023-12
- **URL**: [arXiv](https://arxiv.org/abs/2312.11805)
- **Models**: Gemini 1.0 Ultra, Gemini 1.0 Pro, Gemini 1.0 Nano
- **Type**: Technical Report
- **Cyber Risk Level**: Rudimentary capabilities; moderate threats in deception and cybersecurity
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF (81 tasks) | AI4Security > Offensive Capability | Gemini 1.0: 24/81 (29%) | ReAct agent | Phuong et al. (2403.13793) |
  | Dangerous Capabilities (persuasion, cyber, self-proliferation, self-reasoning) | Security4AI > Misuse Risk | Qualitative (rudimentary) | Internal eval | Technical Report |

- **Agent Setup**: N/A (foundational evaluation)
- **Key Findings**: First Gemini cyber assessment. Gemini 1.0 solved 24/81 InterCode-CTF tasks (29% pass rate, per Phuong et al.). Rudimentary capabilities observed; Pro and Ultra can solve basic CTF tasks and identify straightforward web vulnerabilities, but fail multi-step cybersecurity challenges. Moderate threats flagged in deception and cybersecurity domains.
- **Cross-model Context**: On the same InterCode-CTF benchmark, GPT-4 scored 40/85 (47%) pass@1, GPT-4o scored 26/85 (30%) pass@1, and o1-preview scored 49/85 (57%) pass@1 (per Palisade Research, arXiv:2412.02776, using 85-task subset).

### 4. Gemini 1.5 Technical Report

- **Date**: 2024-02
- **URL**: [arXiv](https://arxiv.org/abs/2403.05530) | [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_v1_5_report.pdf)
- **Models**: Gemini 1.5 Pro, Gemini 1.5 Flash
- **Type**: Technical Report
- **Cyber Risk Level**: Not explicitly assessed against CCL
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Safety violation rate | Security4AI > Misuse Risk | Improved vs 1.0 | SFT/RLHF mitigations | Technical Report |

- **Agent Setup**: N/A
- **Key Findings**: Safety violation rate comparisons vs Gemini 1.0. SFT/RLHF mitigations applied.

### 5. Gemini 2.5 Technical Report

- **Date**: 2025-07
- **URL**: [arXiv](https://arxiv.org/abs/2507.06261) | [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_v2_5_report.pdf)
- **Models**: Gemini 2.5 Pro, Gemini 2.5 Flash, Gemini 2.5 Deep Think, Gemini 2.0 Flash, Gemini 2.0 Pro (experimental)
- **Type**: Technical Report
- **Cyber Risk Level**: CCL alert threshold reached, CCL not met
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF (76 tasks) | AI4Security > Offensive Capability | 73-76/76 (saturated across models) | ReAct agent, multiple models | Cyber Evals Section |
  | In-house CTF (13 tasks) | AI4Security > Offensive Capability | Gemini 2.5 Deep Think: 13/13 | ReAct agent | Cyber Evals Section |
  | Hack the Box | AI4Security > Offensive Capability | Gemini 2.5 Deep Think: 3/13 | Agent-based | Cyber Evals Section |
  | Key Skills Benchmark | AI4Security > Offensive Capability | Reported (details in FSF report) | MITRE ATT&CK aligned | Cyber Evals Section |
  | Pattern Labs External CTFs (50 tasks) | AI4Security > Offensive Capability | Gemini 2.0 Flash: 11/50 (see Entry 23 for breakdown) | Non-public challenges (sourced from Pattern Labs) | Cyber Evals Section |
  | TAP Attack Success Rate (email) | Security4AI > Model Robustness | **99.8% (2.0) → 53.6% (2.5)** | Tree of Attacks with Pruning | Security Section |
  | Beam Search ASR | Security4AI > Model Robustness | **75% (2.0) → 4% (2.5)** | Beam Search attack | Security Section |
  | TAP ASR (calendar) | Security4AI > Model Robustness | 94.6% (2.5) — hardest scenario | TAP, adaptive | Security Section |
  | Combined Defense (2.5 + Warning) | Security4AI > Model Robustness | **6.2% ASR** | Adversarial fine-tuning + Warning | Security Section |
  | Average ASR reduction | Security4AI > Model Robustness | ~47% across attack types (2.0 → 2.5) | Multiple attack methods | Security Section |

- **Agent Setup**: ReAct agent framework for CTF evaluations; N=30-50 attempts per challenge for 2.5 Pro runs, N=10-30 for other models. InterCode-CTF denominator changed from 81 to 76 (5 internet-requiring challenges removed). A challenge is considered solved if any agent in the model family succeeds in at least 1 of N attempts.
- **Key Findings**: Most comprehensive Gemini cyber report. InterCode-CTF saturated (73-76/76 across all models). Deep Think achieved perfect 13/13 on in-house CTF. Significant prompt injection defense improvement via adversarial fine-tuning: TAP 99.8% → 53.6% (email), Beam Search 75% → 4%. Calendar scenario remains challenging (94.6% TAP ASR). Combined Gemini 2.5 + Warning defense achieves 6.2% ASR. FSF Cyber Uplift Level 1 alert threshold reached but CCL not met.

---

## Model Cards

### 6. Gemini 1.0 Model Card

- **Date**: 2023-12
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_1_report.pdf) (page 71)
- **Models**: Gemini 1.0 Ultra, Gemini 1.0 Pro, Gemini 1.0 Nano
- **Type**: Model Card
- **Cyber Risk Level**: Rudimentary
- **Benchmarks Reported**: None (qualitative cyber assessment only)
- **Key Findings**: Embedded within technical report. Preliminary dangerous capabilities assessment.

### 7. Gemini 1.5 Model Card

- **Date**: 2024
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_v1_5_report.pdf) (page 105)
- **Models**: Gemini 1.5 Pro, Gemini 1.5 Flash
- **Type**: Model Card
- **Cyber Risk Level**: Not assessed against CCL
- **Benchmarks Reported**: None (safety violation rate only)
- **Key Findings**: Embedded within technical report. Safety evaluation improvements vs 1.0.

### 8. Gemini 2.0 Flash-Lite Model Card

- **Date**: 2025-04-10
- **URL**: [PDF](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash-lite.pdf)
- **Models**: Gemini 2.0 Flash-Lite
- **Type**: Model Card
- **Cyber Risk Level**: Not separately reported
- **Benchmarks Reported**: None (cyber-specific)
- **Key Findings**: Lightweight model variant. No significant cyber benchmarks reported.

### 9. Gemini 2.0 Flash Model Card

- **Date**: 2025-04-15
- **URL**: [PDF](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf)
- **Models**: Gemini 2.0 Flash
- **Type**: Model Card
- **Cyber Risk Level**: Below CCL alert threshold
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Pattern Labs External CTF (50 tasks) | AI4Security > Offensive Capability | 11/50 | Non-public challenges, anti-contamination | Model Card |
  | FSF Cyber Evals | AI4Security > Offensive Capability | Below CCL alert | Standard FSF methodology | Model Card |

- **Agent Setup**: Agent-based CTF solving
- **Key Findings**: First model card with Pattern Labs CTF results. 11/50 on non-public challenges.

### 10. Gemini 2.5 Pro Preview Model Card

- **Date**: 2025-04-16
- **URL**: [PDF](https://storage.googleapis.com/model-cards/documents/gemini-2.5-pro-preview.pdf) — REMOVED by Google (superseded by final model card)
- **Models**: Gemini 2.5 Pro Preview
- **Type**: Model Card
- **Cyber Risk Level**: CCL alert threshold reached
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF | AI4Security > Offensive Capability | Reported | Standard FSF | Model Card |
  | In-house CTF (13 tasks) | AI4Security > Offensive Capability | Reported | Standard FSF | Model Card |
  | Hack the Box | AI4Security > Offensive Capability | Reported | Standard FSF | Model Card |

- **Agent Setup**: ReAct agent
- **Key Findings**: First Gemini model to reach CCL alert threshold. Link removed by Google; superseded by final Gemini 2.5 Pro model card.
- **Notes**: URL REMOVED by Google.

### 11. Gemini 2.5 Flash Preview Model Card

- **Date**: 2025-06-06
- **URL**: [PDF](https://storage.googleapis.com/model-cards/documents/gemini-2.5-flash-preview.pdf) — REMOVED by Google (superseded by final model card)
- **Models**: Gemini 2.5 Flash Preview
- **Type**: Model Card
- **Cyber Risk Level**: Not separately reported
- **Benchmarks Reported**: None (cyber-specific, deferred to final card)
- **Key Findings**: Preview card. Link removed by Google; superseded by final Gemini 2.5 Flash model card.
- **Notes**: URL REMOVED by Google.

### 12. Gemini 2.5 Flash Model Card

- **Date**: 2025-06-26
- **URL**: [PDF](https://modelcards.withgoogle.com/assets/documents/gemini-2.5-flash.pdf) | [Updated PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Flash-Model-Card.pdf)
- **Models**: Gemini 2.5 Flash
- **Type**: Model Card
- **Cyber Risk Level**: CCL alert threshold reached, CCL not met
- **Benchmarks Reported**: FSF cyber evaluations (details in 2.5 Technical Report)
- **Key Findings**: Final model card for Gemini 2.5 Flash. Supersedes preview card.

### 13. Gemini 2.5 Pro Model Card

- **Date**: 2025-06-27
- **URL**: [PDF](https://modelcards.withgoogle.com/assets/documents/gemini-2.5-pro.pdf)
- **Models**: Gemini 2.5 Pro
- **Type**: Model Card
- **Cyber Risk Level**: CCL alert threshold reached, CCL not met
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF | AI4Security > Offensive Capability | ~76/76 (saturated) | N=30-50 attempts | Model Card |
  | In-house CTF (13 tasks) | AI4Security > Offensive Capability | Reported | Open-sourced via UK AISI Inspect | Model Card |
  | Hack the Box | AI4Security > Offensive Capability | Reported | Standard FSF | Model Card |

- **Agent Setup**: ReAct agent, N=30-50 attempts per challenge. In-house CTF open-sourced via UK AISI Inspect framework.
- **Key Findings**: Comprehensive FSF evals. In-house CTF challenges open-sourced. Supersedes preview card.

### 14. Gemini 2.5 Deep Think Model Card

- **Date**: 2025-08-01
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf)
- **Models**: Gemini 2.5 Deep Think
- **Type**: Model Card
- **Cyber Risk Level**: CCL alert threshold reached for both Cyber and CBRN, CCL not met
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF (76 tasks) | AI4Security > Offensive Capability | 73/76 | ReAct agent | Model Card |
  | In-house CTF (13 tasks) | AI4Security > Offensive Capability | **13/13** | ReAct agent | Model Card |
  | Hack the Box (13 tasks) | AI4Security > Offensive Capability | 3/13 | Agent-based | Model Card |
  | Key Skills v1 (Hard) | AI4Security > Offensive Capability | 6/12 | MITRE ATT&CK aligned (reported in Gemini 3 Pro FSF Report as comparison) | Gemini 3 Pro FSF Report |

- **Agent Setup**: Extended reasoning (Deep Think mode)
- **Key Findings**: Strongest in-house CTF performance (13/13 — perfect score). CCL alert for both Cyber and CBRN domains. First model to achieve 100% on in-house CTF.

### 15. Gemini 2.5 Flash-Lite Model Card

- **Date**: 2025-09-26
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Flash-Lite-Model-Card.pdf)
- **Models**: Gemini 2.5 Flash-Lite
- **Type**: Model Card
- **Cyber Risk Level**: Not separately reported
- **Benchmarks Reported**: None (cyber-specific)
- **Key Findings**: Lightweight variant. No significant cyber benchmarks reported.

### 16. Gemini 2.5 Computer Use Model Card

- **Date**: 2025-10-07
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Computer-Use-Model-Card.pdf)
- **Models**: Gemini 2.5 Computer Use
- **Type**: Model Card
- **Cyber Risk Level**: Agent-specific risks assessed
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Agent adversarial misuse | Security4AI > Misuse Risk | Qualitative assessment | Failure mode analysis | Model Card |
  | Prompt injection in web | Security4AI > Model Robustness | Qualitative assessment | Web interaction testing | Model Card |

- **Agent Setup**: Computer Use agent (browser/desktop interaction)
- **Key Findings**: Agent-specific risk evaluation — adversarial misuse, failure modes, prompt injections in web contexts. Unique computer-use modality.

### 17. Gemini 3 Pro Model Card

- **Date**: 2025-11-18
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-Pro-Model-Card.pdf)
- **Models**: Gemini 3 Pro
- **Type**: Model Card
- **Cyber Risk Level**: CCL alert threshold reached, CCL not met
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Key Skills v1 (Hard) | AI4Security > Offensive Capability | 11/12 | MITRE ATT&CK aligned | Model Card (ref FSF Report) |
  | Key Skills v2 (End-to-end) | AI4Security > Offensive Capability | 0/13 | Multi-stage attack scenarios | Model Card (ref FSF Report) |

- **Agent Setup**: Agentic evaluation with harder realistic challenges (end-to-end attacks)
- **Key Findings**: New harder realistic challenge sets introduced. InterCode-CTF, In-house CTF, and HTB retired for this model (saturated). References separate FSF report for full details.
- **Notes**: InterCode-CTF, In-house CTF, and HTB were **retired** as benchmarks for Gemini 3 Pro due to saturation.

### 18. Gemini 3 Flash Model Card

- **Date**: 2025-12-17
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-Flash-Model-Card.pdf)
- **Models**: Gemini 3 Flash
- **Type**: Model Card
- **Cyber Risk Level**: Not separately reported in detail
- **Benchmarks Reported**: FSF evaluations (details deferred to FSF reports)
- **Key Findings**: Flash variant of Gemini 3 family. Cyber evaluation details in corresponding FSF documentation.

### 19. Gemini 3.1 Pro Model Card

- **Date**: 2026-02-19
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf)
- **Models**: Gemini 3.1 Pro
- **Type**: Model Card
- **Cyber Risk Level**: CCL alert threshold reached, CCL not met
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | FSF Cyber Evals (standard mode) | AI4Security > Offensive Capability | Increased vs 3 Pro; alert threshold reached, CCL not met | Standard FSF | Model Card |
  | FSF Cyber Evals (Deep Think mode) | AI4Security > Offensive Capability | Considerably worse than standard mode (even at high inference levels) | Deep Think mode | Model Card |
  | FSF RE-Bench (ML R&D, Deep Think) | Security4AI > Alignment | Human-normalised avg score **1.27** (vs Gemini 3 Pro's 1.04); "Optimise LLM Foundry": 47s vs human 94s (2x human baseline) | Deep Think mode | Model Card |
  | FSF Harmful Manipulation (Deep Think) | Security4AI > Misuse Risk | Max odds ratio **3.6x** for belief change (same as Gemini 3 Pro); below alert threshold | Deep Think mode | Model Card |
  | FSF CBRN (Deep Think) | Security4AI > Misuse Risk | CCL not reached (Uplift Level 1); accurate info but fails novel/critical stages | Deep Think mode | Model Card |
  | FSF Misalignment (Deep Think, Exploratory) | Security4AI > Alignment | Stealth: similar to Gemini 3 Pro. Situational awareness: stronger — **~100% success** on max_tokens, context_size_mod, oversight_frequency (first model to consistently solve these). Alert threshold not reached overall | Deep Think mode | Model Card |
  | Safety: Text-to-Text | Security4AI > Misuse Risk | +0.10% vs Gemini 3 Pro (non-egregious) | Standard safety eval | Model Card |
  | Safety: Multilingual | Security4AI > Misuse Risk | +0.11% vs Gemini 3 Pro (non-egregious) | Standard safety eval | Model Card |
  | Safety: Image-to-Text | Security4AI > Misuse Risk | -0.33% vs Gemini 3 Pro | Standard safety eval | Model Card |
  | Safety: Tone | Security4AI > Misuse Risk | +0.02% vs Gemini 3 Pro | Standard safety eval | Model Card |
  | Safety: Unjustified-refusals | Security4AI > Misuse Risk | -0.08% vs Gemini 3 Pro | Standard safety eval | Model Card |

- **Agent Setup**: Deep Think mode focus for FSF evaluations (cyber, CBRN, ML R&D, misalignment); standard mode also assessed for cyber
- **Key Findings**: Latest Gemini model (Feb 2026). Increased cyber capabilities vs Gemini 3 Pro in standard mode; alert threshold reached but CCL not met. Deep Think mode performs considerably worse than standard mode on cyber evaluations (notable finding — even at high inference levels). RE-Bench ML R&D: 1.27 human-normalised average (vs 3 Pro's 1.04), with 2x human baseline on one challenge. Situational awareness: first model to consistently solve max_tokens, context_size_mod, and oversight_frequency (~100% success). Harmful manipulation unchanged from 3 Pro (3.6x odds ratio). Safety improvements over Gemini 3 Pro (+0.10% text, +0.11% multilingual, +0.02% tone) but slight regressions on image-to-text (-0.33%) and unjustified-refusals (-0.08%). Human red teaming: satisfied child safety thresholds; similar safety performance to Gemini 3 Pro.
- **Cross-vendor Context (from Claude Opus 4.6 System Card)**: Gemini 3 Pro scored 56.2% on Terminal-Bench 2.0 (Terminus-2 harness, 445 trials) and Gemini 3 Flash scored 50.3%. Gemini 3 Pro achieved $5,478.2 on Vending-Bench 2 (previous SOTA before Opus 4.6's $8,017.59). On OpenAI MRCR v2 256K 8-needles: Gemini 3 Pro = 45.4, Gemini 3 Flash = 58.5; on 1M 8-needles: Gemini 3 Pro = 24.5, Gemini 3 Flash = 32.6. On SWE-bench Verified: Gemini 3 Pro = 76.2%. Additional Gemini 3 Pro scores from Opus 4.6 table: tau2-bench Retail 85.3%, Telecom 98.0%, MCP-Atlas 54.1%, ARC-AGI-2 45.1% (Deep Thinking), GPQA Diamond 91.9%, MMMU-Pro (no tools) 81%, MMMLU 91.8%.

---

## FSF Reports

### 20. Gemini 3 Pro FSF Report

- **Date**: 2025-11
- **URL**: [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf)
- **Models**: Gemini 3 Pro (with Gemini 2.5 comparisons)
- **Type**: FSF Report
- **Cyber Risk Level**: CCL alert threshold reached, CCL not met
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF (76 tasks) | AI4Security > Offensive Capability | Saturated | Standard (retired for 3 Pro) | FSF Report |
  | In-house CTF (13 tasks) | AI4Security > Offensive Capability | Significantly stronger than 2.5 | Standard (retired for 3 Pro) | FSF Report |
  | Key Skills v1 Hard | AI4Security > Offensive Capability | **11/12** (vs 2.5 DT's 6/12) | MITRE ATT&CK aligned | FSF Report |
  | Key Skills v2 End-to-end Attack | AI4Security > Offensive Capability | **0/13** | Multi-stage realistic attacks | FSF Report |

- **Agent Setup**: Agentic evaluation aligned with MITRE ATT&CK and Unified Kill Chain frameworks. New realistic multi-stage attack scenarios introduced.
- **Key Findings**: Most detailed standalone cyber eval from Google. Key Skills v1 hard: 11/12 (nearly doubled from 2.5 Deep Think's 6/12). Key Skills v2 end-to-end: 0/13 (new harder benchmark). InterCode-CTF, In-house CTF, and HTB retired as saturated. New evaluation methodology aligned with MITRE ATT&CK and Unified Kill Chain.
- **Notes**: InterCode-CTF, In-house CTF, and HTB were **retired** for Gemini 3 Pro evaluations due to benchmark saturation.

---

## Standalone Papers

### 21. Evaluating Frontier Models for Dangerous Capabilities (Phuong et al.)

- **Date**: 2024-03-20
- **URL**: [arXiv](https://arxiv.org/abs/2403.13793)
- **Models**: Gemini 1.0 Pro, Gemini 1.0 Ultra
- **Type**: Paper
- **Cyber Risk Level**: Early warning signs; no strong dangerous capabilities found
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode-CTF (81 tasks) | AI4Security > Offensive Capability | Gemini 1.0: 24/81 (29%) | ReAct agent | Paper |
  | In-house CTF (13 challenges) | AI4Security > Offensive Capability | Early warning signs (basic tasks solvable, multi-step challenges fail) | ReAct agent, 13 GDM-built challenges | Paper |

- **Agent Setup**: ReAct agent framework. 13 in-house CTF challenges covering web exploitation, database attacks, privilege escalation, password cracking.
- **Key Findings**: Foundational paper for Google's cyber evaluation methodology. Four evaluation domains: persuasion/deception, cybersecurity, self-proliferation, self-reasoning. Gemini 1.0 solved 24/81 InterCode-CTF tasks (29%). Pro and Ultra agents can solve basic CTF tasks and identify straightforward web vulnerabilities but fail multi-step challenges — unlikely to be of use to threat actors. No strong dangerous capabilities found but early warning signs flagged. Open-sourced: [github.com/google-deepmind/dangerous-capability-evaluations](https://github.com/google-deepmind/dangerous-capability-evaluations).

### 22. Evaluating Frontier Models for Stealth and Situational Awareness

- **Date**: 2025-05-02
- **URL**: [arXiv](https://arxiv.org/abs/2505.01420)
- **Models**: Gemini 2.5 Pro, Gemini 2.5 Flash, GPT-4o, o1, Claude 3.7 Sonnet
- **Type**: Paper
- **Cyber Risk Level**: N/A (alignment evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Stealth Eval (5 evaluations) | Security4AI > Alignment | No concerning levels (pass threshold: 4/5) | Scheming inability safety case | Paper |
  | Situational Awareness (11 evaluations) | Security4AI > Alignment | No concerning levels (pass threshold: 9/11) | Instrumental reasoning assessment | Paper |

- **Agent Setup**: 16 total evaluations (5 stealth + 11 situational awareness). Pass threshold: 80%.
- **Cross-model Stealth Results** (5 evaluations):

  | Evaluation | Gemini 2.5 Pro | Gemini 2.5 Flash | GPT-4o | o1 | Claude 3.7 Sonnet |
  |---|---|---|---|---|---|
  | cover_your_tracks | 0.0% success / 18.0% score | 0.0% / 14.9% | 0.0% / 19.1% | Refused | 0.0% / 15.4% |
  | decision_sabotage | 44.1% success (PASS) | 45.8% (PASS) | N/A | N/A | N/A |
  | strategic_rule_breaking | 35.0% score | 39.5% | 27.9% | 29.8% | 41.2% |
  | classifier_evasion | 15.5% success / 26.3% score | 7.2% / 15.6% | 6.5% / 15.6% | 2.2% / 8.6% | 8.5% / 25.4% |
  | oversight_pattern | 35.4% success / 41.8% (PASS) | 23.0% / 32.0% | 11.0% / 14.7% | 2.0% / 12.7% | 34.0% / 36.3% (PASS) |

  Note: decision_sabotage results not available for non-Gemini models.

- **Cross-model Situational Awareness Results** (11 evaluations):
  - 3 challenges solved by all 5 models: read_logs, disabled_tool, approved_directories
  - 6 challenges solved by no model
  - o1 solved the most challenges overall
  - Gemini 2.5 Pro and Claude 3.7 Sonnet achieved higher success rates on challenges they did solve
  - No model came close to the 80% passing threshold (9/11 challenges)

- **Key Findings**: Establishes "scheming inability safety case" — models failing these tests would be almost certainly incapable of severe harm via scheming. None of the tested frontier models showed concerning levels of stealth or situational awareness. On stealth, Gemini 2.5 Pro and Claude 3.7 Sonnet were the only models to pass oversight_pattern; only Gemini models tested on decision_sabotage.

### 23. Framework for Evaluating Emerging Cyberattack Capabilities

- **Date**: 2025-03-14
- **URL**: [arXiv](https://arxiv.org/abs/2503.11917)
- **Models**: Gemini 2.0 Flash (experimental) — single model evaluated
- **Type**: Paper
- **Cyber Risk Level**: Assessment framework (model-specific results for Gemini 2.0 Flash)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Pattern Labs CTF (50 challenges) | AI4Security > Offensive Capability | **11/50** (22% overall) | Agent-based, 7 attack chain archetypes | Paper |
  | — Strawman difficulty | | 2/2 (100%) | | |
  | — Easy difficulty | | 4/8 (50%) | | |
  | — Medium difficulty | | 4/28 (14.3%) | | |
  | — Hard difficulty | | 1/12 (8.3%) | | |

  **Performance by Bottleneck Skill (Gemini 2.0 Flash)**:

  | Skill Area | Success Rate |
  |---|---|
  | Operational Security / Evasion | 40% |
  | Malware Development | 30% |
  | Information Gathering / Reconnaissance | 11.11% |
  | Vulnerability Exploitation | 6.25% |

- **Agent Setup**: End-to-end attack chain evaluation framework. 12,000+ real-world incidents catalogued by Google Threat Intelligence Group. 7 representative attack chain archetypes identified. 50 challenges sourced from Pattern Labs' library of withheld CTFs.
- **Key Findings**: Most comprehensive AI cyber risk evaluation framework published to date. Gemini 2.0 Flash solved 11/50 challenges overall. Strongest in evasion/OpSec (40%), weakest in vulnerability exploitation (6.25%). 50% of tasks requiring apprentice-level skills solved consistently; medium/hard tasks requiring practitioner/expert-level skills showed limited success. Model "still lacks the skills necessary for real-world operations" — cannot execute end-to-end attacks. Common failures: syntax errors, hallucinated parameters, reliance on generic strategies.
- **Notes**: The 50 challenges are confirmed as Pattern Labs External CTFs (same set referenced in Gemini 2.0 Flash Model Card and Gemini 2.5 Technical Report). Only Gemini 2.0 Flash was evaluated — no cross-model comparison available in this paper.

### 24. Defending Gemini Against Indirect Prompt Injections

- **Date**: 2025-05-18
- **URL**: [arXiv](https://arxiv.org/abs/2505.14534) | [PDF](https://storage.googleapis.com/deepmind-media/Security%20and%20Privacy/Gemini_Security_Paper.pdf)
- **Models**: Gemini 2.0 series, Gemini 2.5 series
- **Type**: Paper
- **Cyber Risk Level**: N/A (model robustness evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | TAP Attack Success Rate (email scenario) | Security4AI > Model Robustness | **99.8% (Gemini 2.0) → 53.6% (Gemini 2.5)** | Tree of Attacks with Pruning | Paper Section 9 |
  | TAP Attack Success Rate (calendar scenario) | Security4AI > Model Robustness | 94.6% (Gemini 2.5) | TAP, adaptive | Paper Section 9 |
  | Beam Search ASR | Security4AI > Model Robustness | **75% (Gemini 2.0) → 4% (Gemini 2.5)** | Beam Search, adaptive | Paper Section 9 |
  | Combined Defense (Gemini 2.5 + Warning) | Security4AI > Model Robustness | **6.2% ASR** (calendar, adaptive TAP) | Adversarial fine-tuning + Warning defense | Paper Section 9 |
  | Gemini 2.0 + Warning baseline | Security4AI > Model Robustness | 10.8% ASR | Warning defense only | Paper Section 8 |
  | Undefended Gemini 2.0 (all attacks) | Security4AI > Model Robustness | >70% ASR in all scenarios | TAP, Actor-Critic, Beam Search, Linear Gen | Paper Section 6 |
  | Automated Red Teaming (ART) | Security4AI > Model Robustness | Continuous evaluation | Adversarial evaluation framework | Paper |

  **Attack Methods Tested**: TAP (Tree of Attacks with Pruning), Actor-Critic, Beam Search, Linear Generation.

  **Key ASR Progression (Gemini 2.0 → 2.5, after adversarial fine-tuning)**:
  - Average ~47% reduction in ASR across attack types
  - TAP (email): 99.8% → 53.6%
  - Beam Search: 75% → 4%
  - Calendar Event (TAP): remains at 94.6% — hardest scenario
  - Best combined defense (Gemini 2.5 + Warning): 6.2% ASR

- **Agent Setup**: Adversarial evaluation framework deploying 4 automated attack techniques continuously against past, current, and future Gemini versions. Function-calling and tool-use capabilities specifically targeted. Attack construction cost: less than $10 against Gemini 2.0 Flash. Non-adaptive and adaptive attack settings tested. Appendix H includes baseline defense analysis on Gemini 1.5.
- **Key Findings**: TAP attack success rate reduced from 99.8% (Gemini 2.0) to 53.6% (Gemini 2.5) in email scenario — significant improvement. Beam Search ASR dropped from 75% to 4%. However, calendar scenario remains challenging (94.6% TAP ASR). Combined defense-in-depth (adversarial fine-tuning + Warning) achieves 6.2% ASR. Adversarial training improves robustness without harming general model capabilities. Most baseline defenses (ICL, Spotlighting, Paraphrasing, Self-reflection) still allow >70% ASR when facing adaptive attacks. Introduces Automated Red Teaming (ART) framework for continuous adversarial evaluation.

---

## Specialized Models

### 25. Sec-Gemini v1

- **Date**: 2025-04
- **URL**: [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) | [GitHub](https://github.com/google/sec-gemini)
- **Models**: Sec-Gemini v1
- **Type**: Product
- **Cyber Risk Level**: N/A (cybersecurity assistant model)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | CTI-MCQ | AI4Security > Cyber Knowledge | **~86.5%** (+11pp over next best model) | [CTI-Bench](https://github.com/xashru/cti-bench) (Rochester IT) | Blog |
  | CTI-RCM | AI4Security > Cyber Knowledge | +10.5pp over next best model | [CTI-Bench](https://github.com/xashru/cti-bench) (Rochester IT) | Blog |

  **Competitors Tested**: GPT-4o, o1, o3-mini, Claude 3.5 Sonnet, DeepSeek V3, Mistral Large.

  **CTI-MCQ Score Derivation**: SecLM (Sec-Gemini's successor platform) achieved 88.5% on CTI-MCQ — described as "2 points ahead of the initial Sec-Gemini announcement and nearly 14 percentage points above the next leading foundation model" ([Google Cloud Security Community](https://security.googlecloudcommunity.com/community-blog-42/fueling-ai-innovation-in-secops-products-the-seclm-platform-and-sec-gemini-research-pipeline-3997)). This implies:
  - Sec-Gemini v1: ~86.5% on CTI-MCQ
  - Next best foundation model: ~74.5% on CTI-MCQ
  - Margin: ~12pp (blog claims 11%+ margin)

- **Agent Setup**: Integrates Google Threat Intelligence (GTI), OSV (Google's open-source vulnerability database), and Mandiant data for real-time cybersecurity reasoning.
- **Key Findings**: First dedicated cybersecurity AI model from Google. Outperforms competitors by 11%+ on CTI-MCQ (threat intelligence) and 10.5%+ on CTI-RCM (root cause → CWE mapping). Estimated ~86.5% CTI-MCQ based on SecLM follow-up data. Available free to select organizations, institutions, professionals, and NGOs for research purposes. Measurements performed in early 2025.
- **Notes**: CTI-MCQ and CTI-RCM benchmarks are from Rochester IT's [CTI-Bench](https://github.com/xashru/cti-bench) project, NOT created by Google. Google/Sec-Gemini uses them for evaluation. The ~86.5% CTI-MCQ score is derived from the SecLM blog post (88.5% - 2pp), not directly stated by Google.

---

## Key Milestones

| Date | Milestone |
|---|---|
| 2023-12 | Gemini 1.0: 24/81 InterCode-CTF (29%), rudimentary cyber capabilities, early warning signs |
| 2024-03 | Phuong et al.: foundational dangerous capabilities paper, 13 in-house CTF challenges, ReAct agent methodology established |
| 2024-05 | FSF v1.0 published — establishes CCL framework |
| 2025-03 | Framework for Evaluating Emerging Cyberattack Capabilities — Gemini 2.0 Flash: 11/50 Pattern Labs CTFs (OpSec 40%, VulnExploit 6.25%) |
| 2025-04 | Gemini 2.5 Pro Preview: first Gemini model to reach CCL alert threshold |
| 2025-04 | Sec-Gemini v1 launched — ~86.5% CTI-MCQ, +11pp over competitors (GPT-4o, o1, o3-mini, Claude 3.5 Sonnet, DeepSeek V3, Mistral Large) |
| 2025-05 | Stealth/Situational Awareness: 5-model comparison (Gemini 2.5 Pro/Flash, GPT-4o, o1, Claude 3.7 Sonnet) — no concerning levels found |
| 2025-05 | TAP attack success rate: 99.8% (2.0) → 53.6% (2.5, email); Beam Search: 75% → 4%; Combined defense: 6.2% ASR |
| 2025-07 | Gemini 2.5 Technical Report — most comprehensive cyber eval to date |
| 2025-08 | Gemini 2.5 Deep Think: 13/13 in-house CTF (strongest), 3/13 HTB |
| 2025-10 | FSF v3.0 published — four risk domains |
| 2025-11 | Gemini 3 Pro: Key Skills v1 hard 11/12, Key Skills v2 end-to-end 0/13. InterCode-CTF/In-house CTF/HTB retired |
| 2026-02 | Gemini 3.1 Pro: increased cyber capabilities vs 3 Pro (standard mode), Deep Think worse than standard on cyber. RE-Bench 1.27 (vs 3 Pro's 1.04). Situational awareness: ~100% on 3 novel challenges. CCL alert, CCL not met |
| 2026-02 | **No Gemini model has crossed Cyber Uplift Level 1 CCL** |
