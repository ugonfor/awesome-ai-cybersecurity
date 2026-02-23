# OpenAI: Cybersecurity Evaluation Documentation

## Overview

- **Total Documents**: 21
- **Date Range**: 2023-03 ~ 2026-02
- **Risk Framework**: Preparedness Framework v2 ([PDF](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf))
- **Backbone Models**: GPT-5.3-Codex, GPT-5.2-Codex
- **Primary Benchmarks**: CTF Challenges, CVE-Bench, Cyber Range, Expert Red Teaming

---

## Frameworks

### 20. Preparedness Framework v2

- **Date**: 2025-04-15
- **URL**: [PDF](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf) | [Blog](https://openai.com/index/updating-our-preparedness-framework/)
- **Models**: N/A (framework document)
- **Type**: Framework
- **Cyber Risk Level**: N/A
- **Benchmarks Reported**: None (defines methodology)
- **Key Findings**: Three Tracked Categories: Cybersecurity, Bio/Chemical, AI Self-improvement. Two thresholds: **High** and **Critical**. High = model automates end-to-end cyber operations against hardened targets OR automates discovery/exploitation of operationally relevant zero-day vulnerabilities.
- **Notes**: Supersedes Preparedness Framework v1 (2023). First applied to o3/o4-mini evaluation (April 2025).

### 21. Strengthening Cyber Resilience Report

- **Date**: 2025-12
- **URL**: [Web](https://openai.com/index/strengthening-cyber-resilience/)
- **Models**: N/A (report covering GPT-5 through GPT-5.2-Codex)
- **Type**: Report
- **Cyber Risk Level**: N/A
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional) | AI4Security > Offensive | 27% → 76% | GPT-5 → GPT-5.1-Codex-Max progression | Report body |
  | CVE-Bench | AI4Security > Offensive | 87% | GPT-5.2-Codex, pass@1 | Report body |

- **Key Findings**: Introduces **Aardvark** (agentic security researcher powered by GPT-5, 92% detection rate on known + synthetic vulnerabilities, 10 CVEs awarded via responsible disclosure). Establishes **Frontier Risk Council** and **Trusted Access for Cyber** program. CTF progression: GPT-5 27% (Aug 2025) → GPT-5.1-Codex-Max 76% (Nov 2025), "more than a twofold increase in just three months."

---

## Model Evaluations

### 1. GPT-4 System Card

- **Date**: 2023-03-23
- **URL**: [PDF](https://cdn.openai.com/papers/gpt-4-system-card.pdf)
- **Models**: GPT-4
- **Type**: System Card
- **Cyber Risk Level**: Low
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Expert Red Teaming | Security4AI > Model Robustness | Qualitative | 50+ external experts, qualitative cyber assessment | System Card |

- **Key Findings**: Not vastly superior to previous LLMs for cyber tasks; useful for social engineering subtasks.

### 2. GPT-4 Technical Report

- **Date**: 2023-03-14
- **URL**: [PDF](https://cdn.openai.com/papers/gpt-4.pdf) | [arXiv:2303.08774](https://arxiv.org/abs/2303.08774)
- **Models**: GPT-4
- **Type**: Technical Report
- **Cyber Risk Level**: Low (references System Card)
- **Benchmarks Reported**: None (references System Card evaluations; describes model-assisted safety pipeline)
- **Key Findings**: Companion to GPT-4 System Card. No independent cybersecurity benchmarks.

### 3. GPT-4o System Card

- **Date**: 2024-08-08
- **URL**: [PDF](https://cdn.openai.com/gpt-4o-system-card.pdf) | [arXiv:2410.21276](https://arxiv.org/abs/2410.21276) | [Blog](https://openai.com/index/gpt-4o-system-card/)
- **Models**: GPT-4o
- **Type**: System Card
- **Cyber Risk Level**: Low
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (High-school) | AI4Security > Offensive | 19% | 172 challenges, 4 categories, 30 rounds tool use, 10 attempts/task, Kali Linux | System Card |
  | Custom CTF (Collegiate) | AI4Security > Offensive | 0% | Same methodology | System Card |
  | Custom CTF (Professional) | AI4Security > Offensive | 1% | Same methodology | System Card |

- **Agent Setup**: Kali Linux environment, 30 rounds of tool use, 10 attempts per task.
- **Key Findings**: Does not meet medium risk threshold. GPT-4o mini shares mitigations but was not separately evaluated.

### 4. OpenAI o1 System Card (September 2024)

- **Date**: 2024-09-12
- **URL**: [PDF](https://cdn.openai.com/o1-system-card.pdf) | [Blog](https://openai.com/index/openai-o1-system-card/)
- **Models**: o1-preview, o1-mini
- **Type**: System Card
- **Cyber Risk Level**: Low
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (High-school) — o1-preview | AI4Security > Offensive | 26.7% | 5 categories, 60 rounds tool use, 12 attempts/task | System Card |
  | Custom CTF (Collegiate) — o1-preview | AI4Security > Offensive | 0% | Same methodology | System Card |
  | Custom CTF (Professional) — o1-preview | AI4Security > Offensive | 2.5% | Same methodology | System Card |
  | Custom CTF (High-school) — o1-mini | AI4Security > Offensive | 28.7% | Same methodology | System Card |
  | Custom CTF (Collegiate) — o1-mini | AI4Security > Offensive | 0% | Same methodology | System Card |
  | Custom CTF (Professional) — o1-mini | AI4Security > Offensive | 3.9% | Same methodology | System Card |

- **Agent Setup**: Kali Linux environment, 60 rounds of tool use, 12 attempts per task.
- **Key Findings**: o1-preview exhibited reward hacking on cybersecurity tasks.

### 5. OpenAI o1 System Card (December 2024)

- **Date**: 2024-12-05
- **URL**: [PDF](https://cdn.openai.com/o1-system-card-20241205.pdf) | [arXiv:2412.16720](https://arxiv.org/abs/2412.16720)
- **Models**: o1, o1-preview, o1-mini
- **Type**: System Card
- **Cyber Risk Level**: Low
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (High-school) — o1 | AI4Security > Offensive | 46.0% | Updated methodology from Sept card | System Card |
  | Custom CTF (Collegiate) — o1 | AI4Security > Offensive | 13.0% | Same methodology | System Card |
  | Custom CTF (Professional) — o1 | AI4Security > Offensive | 13.0% | Same methodology | System Card |

- **Key Findings**: Significant improvement over o1-preview. o1-pro covered under o1 family (same base model + enhanced compute); no separate cyber eval.

### 6. Operator System Card

- **Date**: 2025-01-23
- **URL**: [PDF](https://cdn.openai.com/operator_system_card.pdf) | [Blog](https://openai.com/index/operator-system-card/)
- **Models**: Operator (CUA based on GPT-4o)
- **Type**: System Card
- **Cyber Risk Level**: Low (inherited from GPT-4o)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Prompt Injection Eval | Security4AI > Model Robustness | 99% recall | 77 injection attempts | System Card |
  | Harmful Task Refusal | Security4AI > Misuse Risk | 97% | Refusal rate on harmful prompts | System Card |

- **Key Findings**: CUA-based agent with strong prompt injection defense and harmful task refusal.

### 7. OpenAI o3-mini System Card

- **Date**: 2025-01-31 (updated 2025-02-10)
- **URL**: [PDF](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) | [Blog](https://openai.com/index/o3-mini-system-card/)
- **Models**: o3-mini
- **Type**: System Card
- **Cyber Risk Level**: Low
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (High-school) | AI4Security > Offensive | 61% | 5 categories | System Card |
  | Custom CTF (Collegiate) | AI4Security > Offensive | 21% | Same methodology | System Card |
  | MC Cybersecurity Knowledge — o3-mini | AI4Security > Cyber Knowledge | 53% | Multiple-choice | System Card |
  | MC Cybersecurity Knowledge — o1 | AI4Security > Cyber Knowledge | 59% | Multiple-choice (comparison) | System Card |

- **Key Findings**: MC cybersecurity knowledge shows 18% uplift over GPT-4o.
- **Notes**: o1 score of 59% on MC Cybersecurity Knowledge reported here as comparison baseline.

### 8. Deep Research System Card

- **Date**: 2025-02-25
- **URL**: [PDF](https://cdn.openai.com/deep-research-system-card.pdf) | [Blog](https://openai.com/index/deep-research-system-card/)
- **Models**: Deep Research (o3-based + web browsing)
- **Type**: System Card
- **Cyber Risk Level**: **Medium** (first OpenAI model at this level)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (HS) — no browsing | AI4Security > Offensive | 82% | Without web browsing | System Card |
  | Custom CTF (Coll) — no browsing | AI4Security > Offensive | 55% | Same | System Card |
  | Custom CTF (Pro) — no browsing | AI4Security > Offensive | 47% | Same | System Card |
  | Custom CTF (HS) — w/ browsing | AI4Security > Offensive | 92% | With web browsing enabled | System Card |
  | Custom CTF (Coll) — w/ browsing | AI4Security > Offensive | 91% | Same | System Card |
  | Custom CTF (Pro) — w/ browsing | AI4Security > Offensive | 70% | Same | System Card |
  | Prompt Injection Eval | Security4AI > Model Robustness | Evaluated | For web browsing mode | System Card |

- **Key Findings**: First OpenAI model to reach Medium risk. Web browsing dramatically boosts CTF performance (47% → 70% Professional).

### 9. GPT-4.5 System Card

- **Date**: 2025-02-27
- **URL**: [PDF](https://cdn.openai.com/gpt-4-5-system-card-2272025.pdf) | [Blog](https://openai.com/index/gpt-4-5-system-card/)
- **Models**: GPT-4.5
- **Type**: System Card
- **Cyber Risk Level**: Low
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF | AI4Security > Offensive | — | Same framework as GPT-4o/o1 | System Card |

- **Key Findings**: Evaluated on same CTF framework; remained at Low risk level. No notable cyber capability improvement.

### 10. OpenAI o3 and o4-mini System Card

- **Date**: 2025-04-16
- **URL**: [PDF](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) | [Blog](https://openai.com/index/o3-o4-mini-system-card/)
- **Models**: o3, o4-mini
- **Type**: System Card
- **Cyber Risk Level**: Below High (first evaluated under Preparedness Framework v2)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (HS) — o3 | AI4Security > Offensive | 89% | pass@12 | System Card |
  | Custom CTF (Coll) — o3 | AI4Security > Offensive | 68% | pass@12 | System Card |
  | Custom CTF (Pro) — o3 | AI4Security > Offensive | 59% | pass@12 | System Card |
  | Custom CTF (HS) — o4-mini | AI4Security > Offensive | 80% | pass@12 | System Card |
  | Custom CTF (Coll) — o4-mini | AI4Security > Offensive | 55% | pass@12 | System Card |
  | Custom CTF (Pro) — o4-mini | AI4Security > Offensive | 41% | pass@12 | System Card |
  | Cyber Range — o3 | AI4Security > Offensive | 0% | 2 scenarios, unaided | System Card |
  | Cyber Range — o4-mini | AI4Security > Offensive | 0% | 2 scenarios, unaided | System Card |
  | Irregular External (Pattern Labs) | AI4Security > Offensive | Evaluated | External evaluation | System Card |

- **Agent Setup**: Kali Linux environment, pass@12 methodology.
- **Key Findings**: First models evaluated under Preparedness Framework v2. o3 achieves ~59% on Professional CTF. Cyber Range shows 0% unaided for both models.
- **Notes**: o1 scored 13% on Dec 2024 CTF set; the refactored set used here gives different baselines.

### 11. Codex Addendum (o3/o4-mini)

- **Date**: 2025-05-16
- **URL**: [PDF](https://cdn.openai.com/pdf/8df7697b-c1b2-4222-be00-1fd3298f351d/codex_system_card.pdf) | [Blog](https://openai.com/index/o3-o4-mini-codex-system-card-addendum/)
- **Models**: codex-1 (o3 optimized for SWE)
- **Type**: Addendum
- **Cyber Risk Level**: Below High (inherits o3/o4-mini)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Malware Benchmark | Security4AI > Misuse Risk | Evaluated | Synthetic, large-scale, dual-use prompts | Addendum |

- **Key Findings**: Evaluates codex-1 on malware-related dual-use task benchmark.

### 12. o3 Operator Addendum

- **Date**: 2025
- **URL**: [PDF](https://cdn.openai.com/pdf/4375e605-f9a6-438d-bcc8-190599c183a6/o3_cua_system_card.pdf) | [Blog](https://openai.com/index/o3-o4-mini-system-card-addendum-operator-o3/)
- **Models**: o3 Operator (CUA)
- **Type**: Addendum
- **Cyber Risk Level**: Below High
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Preparedness Framework Evals | Multiple | Evaluated | Cyber, persuasion, CBRN, autonomy | Addendum |

- **Key Findings**: o3 CUA evaluated across all Preparedness Framework risk categories.

### 13. ChatGPT Agent System Card

- **Date**: 2025-07-17
- **URL**: [PDF](https://cdn.openai.com/pdf/6bcccca6-3b64-43cb-a66e-4647073142d7/chatgpt_agent_system_card_launch.pdf)
- **Models**: ChatGPT Agent
- **Type**: System Card
- **Cyber Risk Level**: Not separately rated
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Refactored CTF set | AI4Security > Offensive | Evaluated | Updated with recent CTFs, rebalanced difficulty | System Card |
  | Cyber Range ("Online Retailer") | AI4Security > Offensive | Evaluated | Linux VM, Windows VM, CI/CD, web server, cloud storage | System Card |

- **Agent Setup**: Three-skill framework: exploit discovery, end-to-end attack automation, consistency/scalability.
- **Key Findings**: Introduces refactored CTF set (updated with recent CTFs, rebalanced difficulty) and "Online Retailer" Cyber Range scenario.

### 14. GPT-5 System Card

- **Date**: 2025-08-13
- **URL**: [PDF](https://cdn.openai.com/gpt-5-system-card.pdf) | [arXiv:2601.03267](https://arxiv.org/abs/2601.03267) | [Blog](https://openai.com/index/gpt-5-system-card/)
- **Models**: GPT-5 (gpt-5-thinking, gpt-5-thinking-mini)
- **Type**: System Card
- **Cyber Risk Level**: Below High
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional) | AI4Security > Offensive | ~27% | pass@12, 100+ curated challenges | System Card |
  | Cyber Range — all 5 scenarios | AI4Security > Offensive | 0/30 unaided (all scenarios) | gpt-5-thinking, 30 rollouts each | System Card (Figure 15) |
  | Cyber Range — w/ hints | AI4Security > Offensive | Solves Simple Priv Esc + Azure SSRF infrequently | gpt-5-thinking, pass@1 w/ hints | System Card (Figure 15) |
  | Irregular External — Evasion | AI4Security > Offensive | 51% | Pattern Labs, avg success rate | System Card |
  | Irregular External — Network Attack | AI4Security > Offensive | 49% | Pattern Labs, avg success rate | System Card |
  | Irregular External — Vuln D&E | AI4Security > Offensive | 35% | Pattern Labs, avg success rate | System Card |
  | Irregular External (difficulty) | AI4Security > Offensive | 17/18 easy, 8/14 medium, 0/4 hard | Pattern Labs, difficulty-stratified | System Card |

- **Key Findings**: Professional CTF ~27%. Cyber Range expanded to 5 scenarios but gpt-5-thinking scores 0/30 unaided on all. gpt-5-thinking-mini solves Simple Privilege Escalation twice. Pattern Labs concludes "limited assistance to a moderately skilled cyberoffensive operator."
- **Notes**: CVE-Bench was NOT introduced in GPT-5; it first appears in the GPT-5.1-Codex-Max card. ChatGPT agent achieves highest Collegiate CTF; o3 achieves highest Professional CTF among models compared in this card.

### 15. GPT-5-Codex Addendum

- **Date**: 2025-09-15
- **URL**: [PDF](https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf) | [Blog](https://openai.com/index/gpt-5-system-card-addendum-gpt-5-codex/)
- **Models**: GPT-5-Codex
- **Type**: Addendum
- **Cyber Risk Level**: Below High
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional) | AI4Security > Offensive | ~50% | pass@12 (reported as comparison in GPT-5.1-Codex-Max card) | Addendum / GPT-5.1 card |
  | CVE-Bench | AI4Security > Offensive | 53% | pass@1 (reported as comparison in GPT-5.1-Codex-Max card) | Addendum / GPT-5.1 card |
  | Cyber Range | AI4Security > Offensive | Evaluated | Multi-machine scenarios | Addendum |

- **Key Findings**: Sharp jump from GPT-5 (27% CTF → 50%, CVE-Bench introduced at 53%). Cross-model comparison in GPT-5.1-Codex-Max card provides the specific numbers.

### 16. GPT-5.1-Codex-Max System Card

- **Date**: 2025-11-18
- **URL**: [PDF](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) | [Blog](https://openai.com/index/gpt-5-1-codex-max-system-card/)
- **Models**: GPT-5.1-Codex-Max
- **Type**: System Card
- **Cyber Risk Level**: Below High (most cyber-capable at time)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional) | AI4Security > Offensive | 76% | pass@12; up from 50% (GPT-5-Codex) and 27% (GPT-5) | System Card |
  | CVE-Bench | AI4Security > Offensive | 80% | pass@1; up from 53% (GPT-5-Codex) | System Card |
  | Cyber Range | AI4Security > Offensive | 7/8 scenarios (81.8% combined) | Solved Leaked Token via unintended misconfiguration; 81.8% from GPT-5.2-Codex cross-model comparison | System Card / GPT-5.2-Codex addendum |
  | Irregular External — Network Attack | AI4Security > Offensive | 37% | Pattern Labs, average success rate | System Card |
  | Irregular External — Vuln Discovery | AI4Security > Offensive | 41% | Pattern Labs, average success rate | System Card |
  | Irregular External — Evasion | AI4Security > Offensive | 43% | Pattern Labs, average success rate | System Card |
  | Irregular External (difficulty) | AI4Security > Offensive | 17/18 easy, 9/17 medium, 0/6 hard | Pattern Labs, difficulty-stratified | System Card |

- **Key Findings**: Major leap from GPT-5-Codex (50% → 76% CTF; 53% → 80% CVE-Bench). Cyber Range first shows meaningful scores (7/8 scenarios). Leaked Token solved via unintended misconfiguration (partially solving intended attack path). Pattern Labs external eval concludes "limited assistance to a moderately skilled cyberoffensive operator."
- **Notes**: GPT-5-Codex comparison baselines (CTF 50%, CVE-Bench 53%) reported here as cross-model reference.

### 17. GPT-5.2 System Card Update

- **Date**: 2025-12-11
- **URL**: [PDF](https://cdn.openai.com/pdf/3a4153c8-c748-4b71-8e31-aecbde944f8d/oai_5_2_system-card.pdf) | [Blog](https://openai.com/index/gpt-5-system-card-update-gpt-5-2/)
- **Models**: GPT-5.2
- **Type**: System Card
- **Cyber Risk Level**: Below High
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional) — GPT-5.2-Thinking | AI4Security > Offensive | 82% | pass@12 (reported in GPT-5.2-Codex addendum comparison) | System Card / GPT-5.2-Codex addendum |
  | Custom CTF (Professional, xhigh) — GPT-5.2-Thinking | AI4Security > Offensive | 67.7% | xhigh compute (reported in GPT-5.3-Codex cross-model comparison) | GPT-5.3-Codex System Card |
  | CVE-Bench — GPT-5.2-Thinking | AI4Security > Offensive | 69% | pass@1 (reported in GPT-5.2-Codex addendum comparison) | System Card / GPT-5.2-Codex addendum |
  | Cyber Range — GPT-5.2-Thinking | AI4Security > Offensive | 63.6% | Combined pass rate (reported in GPT-5.2-Codex addendum comparison) | System Card / GPT-5.2-Codex addendum |

- **Key Findings**: Introduced "safe-completions" for dual-use cybersecurity queries. gpt-5.2-thinking performs considerably better than gpt-5-thinking and is at a similar capability level as gpt-5.1-codex-max. CTF improved (76% → 82%) but CVE-Bench declined (80% → 69%) compared to GPT-5.1-Codex-Max.
- **Notes**: Cross-model scores sourced from GPT-5.2-Codex addendum comparison table.

### 18. GPT-5.2-Codex Addendum

- **Date**: 2025-12-18
- **URL**: [PDF](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) | [Blog](https://openai.com/index/gpt-5-2-codex-system-card/)
- **Models**: GPT-5.2-Codex
- **Type**: Addendum
- **Cyber Risk Level**: Below High (strongest at time)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional) | AI4Security > Offensive | 88% | pass@12; strongest at time of release | Addendum |
  | Custom CTF (Professional, xhigh) | AI4Security > Offensive | 67.4% | xhigh compute (reported in GPT-5.3-Codex cross-model comparison) | GPT-5.3-Codex System Card |
  | CVE-Bench (Blind 0-day) | AI4Security > Offensive | 87% | pass@1 | Addendum |
  | Cyber Range (Combined) | AI4Security > Offensive | 72.7% | Combined pass rate | Addendum |
  | — Cross-model: GPT-5.1-Codex-Max CTF | AI4Security > Offensive | 76% | pass@12 (comparison baseline) | Addendum |
  | — Cross-model: GPT-5.1-Codex-Max CVE-Bench | AI4Security > Offensive | 80% | pass@1 (comparison baseline) | Addendum |
  | — Cross-model: GPT-5.1-Codex-Max Cyber Range | AI4Security > Offensive | 81.8% | Combined pass rate (comparison baseline) | Addendum |
  | — Cross-model: GPT-5.2-Thinking CTF | AI4Security > Offensive | 82% | pass@12 (comparison baseline) | Addendum |
  | — Cross-model: GPT-5.2-Thinking CVE-Bench | AI4Security > Offensive | 69% | pass@1 (comparison baseline) | Addendum |
  | — Cross-model: GPT-5.2-Thinking Cyber Range | AI4Security > Offensive | 63.6% | Combined pass rate (comparison baseline) | Addendum |

- **Key Findings**: CTF 88% (strongest), CVE-Bench 87%, Cyber Range 72.7%. "Current trends suggest models may cross High threshold in near future." Compaction (coherent work across multiple context windows) cited as key for CTF performance.
- **Notes**: Full cross-model comparison table found in addendum. GPT-5.2-Codex surpasses GPT-5.1-Codex-Max on CTF (88% vs 76%) and CVE-Bench (87% vs 80%) but trails on Cyber Range (72.7% vs 81.8%). GPT-5.2-Thinking shows CTF gain (82%) but CVE-Bench regression (69%) vs GPT-5.1-Codex-Max (80%).

### 19. GPT-5.3-Codex System Card

- **Date**: 2026-02-05
- **URL**: [PDF](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) | [Blog](https://openai.com/index/gpt-5-3-codex-system-card/)
- **Models**: GPT-5.3-Codex, GPT-5.3-Codex-Spark
- **Type**: System Card
- **Cyber Risk Level**: **HIGH (precautionary)** — "We do not have definitive evidence that this model reaches our High threshold, but are taking a precautionary approach." First OpenAI model at this level.
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (Professional, xhigh) | AI4Security > Offensive | 77.6% | pass@12, xhigh compute; matches GPT-5.2-Codex on peak CTF | System Card |
  | CVE-Bench | AI4Security > Offensive | 90% | pass@1, 34/40 challenges, zero-day config | System Card |
  | Cyber Range | AI4Security > Offensive | 80% | 12/15 scenarios, pass/fail over 16 trials | System Card |
  | Irregular External — Network Attack | AI4Security > Offensive | 86% | Pattern Labs external eval | System Card |
  | Irregular External — Vuln D&E | AI4Security > Offensive | 72% | Pattern Labs external eval | System Card |
  | Irregular External — Evasion | AI4Security > Offensive | 53% | Pattern Labs external eval | System Card |
  | Irregular External — CyScenarioBench | AI4Security > Offensive | 0% | Pattern Labs, complex branching missions | System Card |
  | — Cross-model: GPT-5.2-Codex CTF (xhigh) | AI4Security > Offensive | 67.4% | pass@12, xhigh (comparison) | System Card |
  | — Cross-model: GPT-5.2 CTF (xhigh) | AI4Security > Offensive | 67.7% | pass@12, xhigh (comparison) | System Card |

- **Agent Setup**: First model to pass all thresholds across all three core evaluations (CTF, CVE-Bench, Cyber Range). Identified attack paths, reverse-engineered binaries, and executed exploits end-to-end without explicit guidance.
- **Key Findings**: First OpenAI model rated HIGH. CTF 77.6% (xhigh), CVE-Bench 90%, Cyber Range 80% (12/15). Failed Cyber Range scenarios: EDR Evasion, CA/DNS Hijacking, Leaked Token (patched after GPT-5.2-Codex). CyScenarioBench 0% (autonomous end-to-end hacking campaigns remain unsolved). GPT-5.3-Codex-Spark rated Below High.
- **Notes**: CTF score of 77.6% uses "xhigh" compute setting. The comparison shows GPT-5.2-Codex at 67.4% and GPT-5.2 at 67.7% under the same xhigh methodology. Note this differs from the pass@12 scores in the GPT-5.2-Codex addendum (88%) which used standard methodology.

---

## Cyber Risk Progression

| Model | Date | Risk Level | Professional CTF | CVE-Bench | Cyber Range | Irregular (NAS/VDE/Evasion) |
|---|---|---|---|---|---|---|
| GPT-4 | 2023-03 | Low | Qualitative only | — | — | — |
| GPT-4o | 2024-08 | Low | 1% | — | — | — |
| o1-preview | 2024-09 | Low | 2.5% | — | — | — |
| o1-mini | 2024-09 | Low | 3.9% | — | — | — |
| o1 | 2024-12 | Low | 13% | — | — | — |
| o3-mini | 2025-01 | Low | HS 61%, Coll 21% | — | — | — |
| Deep Research (no browse) | 2025-02 | Medium | 47% | — | — | — |
| Deep Research (w/ browse) | 2025-02 | Medium | 70% | — | — | — |
| GPT-4.5 | 2025-02 | Low | — | — | — | — |
| o3 | 2025-04 | Below High | ~59% (pass@12) | — | 0% (2 scenarios) | — |
| o4-mini | 2025-04 | Below High | ~41% (pass@12) | — | 0% (2 scenarios) | — |
| GPT-5 | 2025-08 | Below High | ~27% (pass@12) | — | 0/30 unaided (5 scenarios) | 49%/35%/51% |
| GPT-5-Codex | 2025-09 | Below High | ~50% | 53% | Evaluated | — |
| GPT-5.1-Codex-Max | 2025-11 | Below High | 76% | 80% | 7/8 scenarios | 37%/41%/43% |
| GPT-5.2-Thinking | 2025-12 | Below High | 82% | 69% | 63.6% | — |
| GPT-5.2-Codex | 2025-12 | Below High | 88% | 87% | 72.7% | — |
| GPT-5.3-Codex | 2026-02 | **HIGH** | 77.6% (xhigh) | 90% | 80% (12/15) | 86%/72%/53% |

---

## Key Milestones

| Date | Milestone |
|---|---|
| 2023-03 | GPT-4 System Card: first cybersecurity evaluation (qualitative, expert red teaming) |
| 2024-08 | GPT-4o System Card: first quantitative CTF benchmarks (172 challenges, 3 difficulty levels) |
| 2024-12 | o1 reaches 13% Professional CTF (first double-digit performance) |
| 2025-02 | Deep Research becomes first OpenAI model rated **Medium** risk; 70% Professional CTF with browsing |
| 2025-04 | Preparedness Framework v2 published; o3/o4-mini rated "Below High" (new category) |
| 2025-07 | ChatGPT Agent introduces refactored CTF set and Cyber Range "Online Retailer" scenario |
| 2025-08 | GPT-5 introduces expanded Cyber Range (5 scenarios); 0/30 unaided on all; Pattern Labs external eval (49%/35%/51%) |
| 2025-09 | GPT-5-Codex sharp jump: CTF ~50%, CVE-Bench 53% (first CVE-Bench scores) |
| 2025-11 | GPT-5.1-Codex-Max reaches 76% CTF, 80% CVE-Bench, 7/8 Cyber Range scenarios |
| 2025-12 | GPT-5.2-Codex hits 88% CTF, 87% CVE-Bench, 72.7% Cyber Range; "safe-completions" introduced; Strengthening Cyber Resilience report published with Aardvark, Frontier Risk Council, Trusted Access for Cyber |
| 2026-02 | GPT-5.3-Codex rated **HIGH** (precautionary) — first OpenAI model at this level; CTF 77.6% (xhigh), CVE-Bench 90%, Cyber Range 80% (12/15), Pattern Labs 86%/72%/53% |

---

## Notes

- **GPT-3.5**: No standalone system card with cybersecurity benchmarks.
- **GPT-4o mini**: No separate system card; shares GPT-4o mitigations.
- **o1-pro**: Covered under o1 System Card (Dec 2024); no separate cyber eval.
- **US/UK AISI Joint Test for o1**: [PDF](https://www.nist.gov/system/files/documents/2024/12/18/US_UK_AI%20Safety%20Institute_%20December_Publication-OpenAIo1.pdf)
- **CTF methodology note**: GPT-5.3-Codex card uses "xhigh" compute setting for CTF, yielding 77.6%. The GPT-5.2-Codex addendum uses standard pass@12, yielding 88%. These are NOT directly comparable. Under xhigh, GPT-5.2-Codex scores 67.4% (vs 88% standard).
- **Irregular/Pattern Labs**: External evaluation by Pattern Labs (formerly Irregular). NAS = Network Attack Simulation, VDE = Vulnerability Discovery & Exploitation. CyScenarioBench (complex branching missions) remains at 0% even for GPT-5.3-Codex.
- **Cyber Range scenario count**: Expanded from 2 (o3/o4-mini era) → 5 (GPT-5 era) → 8 (GPT-5.1-Codex-Max era) → 15 (GPT-5.3-Codex era). Leaked Token scenario patched between GPT-5.2-Codex and GPT-5.3-Codex.
- **Data sources for this update**: arXiv:2601.03267 (GPT-5 system card), thezvi.substack.com (GPT-5.1-Codex-Max analysis), binaryverseai.com (GPT-5.2-Codex benchmark table), macobserver.com + digitalapplied.com + cometapi.com (GPT-5.3-Codex scores), ignorance.ai (GPT-5.3-Codex Pattern Labs data), xugj520.cn (Strengthening Cyber Resilience mirror).
