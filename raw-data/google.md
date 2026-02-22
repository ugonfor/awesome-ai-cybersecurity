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
  | Dangerous Capabilities (persuasion, cyber, self-proliferation, self-reasoning) | Security4AI > Misuse Risk | Qualitative (rudimentary) | Internal eval | Technical Report |

- **Agent Setup**: N/A (foundational evaluation)
- **Key Findings**: First Gemini cyber assessment. Rudimentary capabilities observed; moderate threats flagged in deception and cybersecurity domains.

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
  | Pattern Labs External CTFs (50 tasks) | AI4Security > Offensive Capability | Gemini 2.0 Flash: 11/50 | Non-public challenges | Cyber Evals Section |
  | TAP Attack Success Rate | Security4AI > Model Robustness | 99.8% (2.0) → 53.6% (2.5) | Tree of Attacks with Pruning | Security Section |
  | Indirect Prompt Injection | Security4AI > Model Robustness | Significant improvement 2.0→2.5 | Adversarial evaluation | Security Section |

- **Agent Setup**: ReAct agent framework for CTF evaluations; N=30-50 attempts per challenge
- **Key Findings**: Most comprehensive Gemini cyber report. InterCode-CTF saturated. Deep Think achieved perfect 13/13 on in-house CTF. Significant prompt injection defense improvement (TAP 99.8% → 53.6%). FSF Cyber Uplift Level 1 alert threshold reached but CCL not met.

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
  | FSF Cyber Evals (Deep Think mode focus) | AI4Security > Offensive Capability | Increased vs 3 Pro | Standard FSF + Deep Think | Model Card |

- **Agent Setup**: Deep Think mode focus for cyber evaluations
- **Key Findings**: Latest Gemini model (Feb 2026). Increased cyber capabilities vs Gemini 3 Pro. Cyber Uplift Level 1 alert threshold reached, CCL not met. Deep Think mode specifically assessed for cyber capabilities.

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
  | In-house CTF (13 challenges) | AI4Security > Offensive Capability | Early warning signs | ReAct agent, 13 GDM-built challenges | Paper |

- **Agent Setup**: ReAct agent framework. 13 in-house CTF challenges covering web exploitation, database attacks, privilege escalation, password cracking.
- **Key Findings**: Foundational paper for Google's cyber evaluation methodology. Four evaluation domains: persuasion/deception, cybersecurity, self-proliferation, self-reasoning. No strong dangerous capabilities found but early warning signs flagged. Open-sourced: [github.com/google-deepmind/dangerous-capability-evaluations](https://github.com/google-deepmind/dangerous-capability-evaluations).

### 22. Evaluating Frontier Models for Stealth and Situational Awareness

- **Date**: 2025-05-02
- **URL**: [arXiv](https://arxiv.org/abs/2505.01420)
- **Models**: Gemini 2.5 Pro, Gemini 2.5 Flash, GPT-4o, o1, Claude 3.7 Sonnet
- **Type**: Paper
- **Cyber Risk Level**: N/A (alignment evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Stealth Eval (5 evaluations) | Security4AI > Alignment | No concerning levels | Scheming inability safety case | Paper |
  | Situational Awareness (11 evaluations) | Security4AI > Alignment | No concerning levels | Instrumental reasoning assessment | Paper |

- **Agent Setup**: 16 total evaluations (5 stealth + 11 situational awareness)
- **Key Findings**: Establishes "scheming inability safety case" — models failing these tests would be almost certainly incapable of severe harm via scheming. None of the tested frontier models showed concerning levels of stealth or situational awareness.

### 23. Framework for Evaluating Emerging Cyberattack Capabilities

- **Date**: 2025-03-14
- **URL**: [arXiv](https://arxiv.org/abs/2503.11917)
- **Models**: Gemini 2.0 Flash (experimental) + others
- **Type**: Paper
- **Cyber Risk Level**: Assessment framework (not model-specific)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | 50 new cyberattack challenges | AI4Security > Offensive Capability | Framework-level assessment | 7 attack chain archetypes, 12,000+ real incidents | Paper |

- **Agent Setup**: End-to-end attack chain evaluation framework. 12,000+ real-world incidents catalogued by Google Threat Intelligence Group. 7 representative attack chain archetypes identified.
- **Key Findings**: Most comprehensive AI cyber risk evaluation framework published to date. Bottleneck analysis identifying phases most susceptible to AI-driven disruption. 50 new externally-developed challenges. Recommendations for defense prioritization.

### 24. Defending Gemini Against Indirect Prompt Injections

- **Date**: 2025-05-18
- **URL**: [arXiv](https://arxiv.org/abs/2505.14534) | [PDF](https://storage.googleapis.com/deepmind-media/Security%20and%20Privacy/Gemini_Security_Paper.pdf)
- **Models**: Gemini 2.0 series, Gemini 2.5 series
- **Type**: Paper
- **Cyber Risk Level**: N/A (model robustness evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | TAP Attack Success Rate | Security4AI > Model Robustness | 99.8% (Gemini 2.0) → 53.6% (Gemini 2.5) | Tree of Attacks with Pruning | Paper |
  | Automated Red Teaming (ART) | Security4AI > Model Robustness | Continuous evaluation | Adversarial evaluation framework | Paper |

- **Agent Setup**: Adversarial evaluation framework deploying suite of adaptive attack techniques continuously against past, current, and future Gemini versions. Function-calling and tool-use capabilities specifically targeted.
- **Key Findings**: TAP attack success rate reduced from 99.8% (Gemini 2.0) to 53.6% (Gemini 2.5) — significant improvement. Introduces Automated Red Teaming (ART) framework for continuous adversarial evaluation. Addresses indirect prompt injection in function-calling/tool-use contexts.

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
  | CTI-MCQ | AI4Security > Cyber Knowledge | +11% over competitors | [CTI-Bench](https://github.com/xashru/cti-bench) (Rochester IT) | Blog |
  | CTI-RCM | AI4Security > Cyber Knowledge | +10.5% over competitors | [CTI-Bench](https://github.com/xashru/cti-bench) (Rochester IT) | Blog |

- **Agent Setup**: Integrates Google Threat Intelligence (GTI), OSV (Google's open-source vulnerability database), and Mandiant data for real-time cybersecurity reasoning.
- **Key Findings**: First dedicated cybersecurity AI model from Google. Outperforms competitors by 11%+ on CTI-MCQ (threat intelligence) and 10.5%+ on CTI-RCM (root cause → CWE mapping). Available free to select organizations, institutions, professionals, and NGOs for research purposes.
- **Notes**: CTI-MCQ and CTI-RCM benchmarks are from Rochester IT's [CTI-Bench](https://github.com/xashru/cti-bench) project, NOT created by Google. Google/Sec-Gemini uses them for evaluation.

---

## Key Milestones

| Date | Milestone |
|---|---|
| 2023-12 | Gemini 1.0: rudimentary cyber capabilities, early warning signs |
| 2024-03 | Phuong et al.: foundational dangerous capabilities paper, 13 in-house CTF challenges, ReAct agent methodology established |
| 2024-05 | FSF v1.0 published — establishes CCL framework |
| 2025-03 | Framework for Evaluating Emerging Cyberattack Capabilities — 12,000+ real incidents, 50 new challenges |
| 2025-04 | Gemini 2.5 Pro Preview: first Gemini model to reach CCL alert threshold |
| 2025-04 | Sec-Gemini v1 launched — +11% CTI-MCQ, +10.5% CTI-RCM over competitors |
| 2025-05 | TAP attack success rate: 99.8% (2.0) → 53.6% (2.5) |
| 2025-07 | Gemini 2.5 Technical Report — most comprehensive cyber eval to date |
| 2025-08 | Gemini 2.5 Deep Think: 13/13 in-house CTF (strongest), 3/13 HTB |
| 2025-10 | FSF v3.0 published — four risk domains |
| 2025-11 | Gemini 3 Pro: Key Skills v1 hard 11/12, Key Skills v2 end-to-end 0/13. InterCode-CTF/In-house CTF/HTB retired |
| 2026-02 | Gemini 3.1 Pro: increased capabilities vs 3 Pro, CCL alert, CCL not met |
| 2026-02 | **No Gemini model has crossed Cyber Uplift Level 1 CCL** |
