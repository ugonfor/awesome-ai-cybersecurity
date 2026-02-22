# AI4Security — Offensive Capability Benchmarks

> AI performing offensive cybersecurity tasks: CTF solving, vulnerability exploitation, penetration testing.

---

### [Cybench](https://cybench.github.io/)
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Stanford University
- **Used by**: Anthropic, xAI (spells it "CyBench"), UK AISI, US AISI
- **Scale**: 40 professional-level CTF tasks from 4 competitions (HackTheBox, SekaiCTF, Glacier, HKCert)
- **Dataset**: Open
- **Reference**: [Cybench: A Framework for Evaluating Cybersecurity Capabilities and Risks of Language Models](https://arxiv.org/abs/2408.08926)
- **Summary**: Professional CTF benchmark covering pwn, crypto, web, reverse engineering, forensics, and misc. Evaluated via UK AISI Inspect framework. Used in US/UK AISI joint pre-deployment tests on Claude 3.5 Sonnet and OpenAI o1.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude 3.7 Sonnet | 35.9% | 2025.02 | [System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
  | Claude Sonnet 4.5 | 76.5% | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
  | Grok 4 | Below human professional | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4.1 | Substantially below human experts | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### [CyberGym](https://red.anthropic.com/2025/ai-for-cyber-defenders/)
- **Category**: AI4Security > Offensive Capability > Vulnerability Discovery
- **Created by**: UC Berkeley (Center for Responsible, Decentralized Intelligence)
- **Used by**: Anthropic
- **Scale**: 1,507 vulnerabilities across 188 open-source projects
- **Dataset**: Open
- **Summary**: Real-world vulnerability detection benchmark using actual CVEs in open-source codebases, measuring AI's ability to find and reproduce vulnerabilities.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude Sonnet 4 | Strongest on public leaderboard | 2025 | [Frontier Red Team](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
  | Claude Sonnet 4.5 | 28.9% ($2 cost), 66.7% vuln reproduction (30 trials) | 2025.09 | [Frontier Red Team](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |

---

### CVE-Bench
- **Category**: AI4Security > Offensive Capability > Vulnerability Exploitation
- **Created by**: OpenAI
- **Used by**: OpenAI
- **Scale**: Real-world web application CVEs
- **Dataset**: Closed
- **Summary**: Benchmark for exploiting real-world web application vulnerabilities (actual CVEs), measured with pass@1 metric.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | GPT-5.2-Codex | 87% (pass@1) | 2025.12 | [Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |

---

### OpenAI CTF Challenges
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: OpenAI
- **Used by**: OpenAI
- **Scale**: 172 challenges across high-school, collegiate, and professional levels (web exploit, RE, pwn, crypto, misc)
- **Dataset**: Closed
- **Summary**: OpenAI's proprietary CTF suite with three difficulty tiers. Models use Kali Linux with 30-60 rounds of tool use and 10-12 attempts per task.
- **Results**:
  | Model | HS | Collegiate | Professional | Date | Source |
  |---|---|---|---|---|---|
  | GPT-4o | 19% | 0% | 1% | 2024.08 | [System Card](https://cdn.openai.com/gpt-4o-system-card.pdf) |
  | o1-preview | 26.7% | 0% | 2.5% | 2024.09 | [System Card](https://cdn.openai.com/o1-system-card.pdf) |
  | o1 | 46% | 13% | 13% | 2024.12 | [System Card](https://cdn.openai.com/o1-system-card-20241205.pdf) |
  | o3-mini | 61% | 21% | — | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
  | Deep Research (no browse) | 82% | 55% | 47% | 2025.02 | [System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
  | Deep Research (w/ browse) | 92% | 91% | 70% | 2025.02 | [System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
  | o3 | — | — | ~58% | 2025.04 | [System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
  | GPT-5 | — | — | ~27% (pass@12) | 2025.08 | [System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
  | GPT-5.1-Codex-Max | — | — | ~76% | 2025.11 | [System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
  | GPT-5.3-Codex | — | — | All passed | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |

---

### Cyber Range
- **Category**: AI4Security > Offensive Capability > End-to-End Attack
- **Created by**: OpenAI, Anthropic (independently)
- **Used by**: OpenAI, Anthropic
- **Scale**: 5+ multi-machine network scenarios (OpenAI); ~50-host networks (Anthropic/CMU)
- **Dataset**: Closed
- **Summary**: Realistic multi-machine network attack scenarios testing end-to-end offensive capabilities including network infiltration, lateral movement, and privilege escalation.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | GPT-5.1-Codex-Max | Network Attack 37%, Vuln Discovery 41%, Evasion 43% | 2025.11 | [System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
  | GPT-5.3-Codex | All except 3 scenarios | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | Claude Sonnet 4.5 | Equifax Simulation: 2/5 autonomous | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |

---

### [InterCode-CTF](https://arxiv.org/abs/2306.14898)
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Princeton University
- **Used by**: Google
- **Scale**: 76 easy CTF challenges
- **Dataset**: Open
- **Reference**: [InterCode: Standardizing and Benchmarking Interactive Coding with Execution Feedback](https://arxiv.org/abs/2306.14898)
- **Summary**: Easy-level CTF benchmark; largely saturated by frontier models. Part of Google's FSF evaluation suite.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Gemini 2.5 Deep Think | 73/76 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
  | Gemini 2.5 Pro | 76/76 (saturated) | 2025.06 | [Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2.5-pro.pdf) |

---

### [In-house CTF (Google DeepMind)](https://github.com/google-deepmind/dangerous-capability-evaluations)
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 13 medium-difficulty challenges (web, exploits, DB, privesc, passwords)
- **Dataset**: Open (via UK AISI Inspect framework)
- **Reference**: [Evaluating Frontier Models for Dangerous Capabilities](https://arxiv.org/abs/2403.13793)
- **Summary**: Medium-difficulty CTF suite built by GDM, open-sourced through UK AISI Inspect. Uses ReAct agent framework.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Gemini 2.5 Deep Think | 13/13 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |

---

### Hack the Box
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Hack The Box (platform)
- **Used by**: Google, Anthropic
- **Scale**: 12-13 professional-level challenges
- **Dataset**: Partial (commercial platform)
- **Summary**: Professional-grade CTF challenges from the Hack The Box platform, used to evaluate AI on hard real-world challenges.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Gemini 2.5 Deep Think | 3/13 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
  | Gemini 3 Pro | 11/12 | 2025.11 | [FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
  | Claude (HackTheBox AI vs Human) | 19/20, 30th/161 | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

---

### Key Skills Benchmark
- **Category**: AI4Security > Offensive Capability > Skill Assessment
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: Multiple skill categories (recon, tool dev, tool use, OPSEC)
- **Dataset**: Closed
- **Summary**: MITRE ATT&CK-aligned skill evaluation measuring specific offensive capabilities: reconnaissance, tool development, tool usage, and operational security.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Gemini 3 Pro | Almost all hard challenges completed | 2025.11 | [FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |

---

### Pattern Labs External CTFs
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Pattern Labs (for Google)
- **Used by**: Google
- **Scale**: 50 non-public challenges
- **Dataset**: Closed (anti-contamination design)
- **Summary**: External CTF challenges specifically designed to prevent data contamination, providing unbiased evaluation of model capabilities.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Gemini 2.0 Flash | 11/50 | 2025.04 | [Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf) |

---

### CMU Cyber Ranges
- **Category**: AI4Security > Offensive Capability > End-to-End Attack
- **Created by**: Carnegie Mellon University / Anthropic
- **Used by**: Anthropic
- **Scale**: ~50-host network simulations
- **Dataset**: Closed
- **Summary**: Large-scale network simulations for evaluating end-to-end attack chains, including lateral movement and privilege escalation.

---

### Equifax Simulation
- **Category**: AI4Security > Offensive Capability > End-to-End Attack
- **Created by**: Anthropic (Frontier Red Team)
- **Used by**: Anthropic
- **Scale**: High-fidelity breach simulation (1 scenario, 5 trials)
- **Dataset**: Closed
- **Summary**: Simulated recreation of the Equifax breach to test autonomous end-to-end exploitation capabilities.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude Sonnet 4.5 | 2/5 autonomous success | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |

---

### Real CTF Competitions (Anthropic)
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Various competition organizers
- **Used by**: Anthropic
- **Scale**: Multiple live competitions
- **Dataset**: Open (public competitions)
- **Reference**: [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/)
- **Summary**: Claude entered real-world CTF competitions against human teams to measure practical offensive capability.
- **Results**:
  | Competition | Score | Source |
  |---|---|---|
  | PicoCTF 2025 | 297th/10,460 (top 3%), 32/41 challenges | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
  | HackTheBox AI vs Human | 30th/161, 4th/8 AI teams, 19/20 challenges | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
  | WRCCDC | 6th/9 teams | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

---

### Zero-day Discovery Evaluation
- **Category**: AI4Security > Offensive Capability > Vulnerability Discovery
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: Pre-release testing against open-source software
- **Dataset**: Closed
- **Summary**: Evaluation of model's ability to discover novel, previously unknown vulnerabilities in real software.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude Opus 4.6 | 500+ novel vulnerabilities | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

---

## Academic Benchmarks (Community-Driven)

> The following benchmarks originate from the academic community and are not primarily used in the four major vendors' official model evaluations.

---

### [NYU CTF Bench](https://github.com/NYU-LLM-CTF/NYU_CTF_Bench)
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: New York University
- **Used by**: Academic community
- **Scale**: 200 challenges across 6 categories (web, pwn, forensics, reverse engineering, crypto, misc)
- **Dataset**: Open
- **Reference**: [NYU CTF Bench: A Scalable Open-Source Benchmark Dataset for Evaluating LLMs in Offensive Security](https://arxiv.org/abs/2406.05590)
- **Summary**: First open-source CTF benchmark for LLM offensive security evaluation with fully automated framework and tool-calling support. NeurIPS 2024 Datasets and Benchmarks Track.

---

### [CTFusion](https://openreview.net/forum?id=2zQJHLbyqM)
- **Category**: AI4Security > Offensive Capability > CTF (Live)
- **Created by**: Academic researchers
- **Used by**: Academic community
- **Scale**: Streaming evaluation across 5+ live CTF competitions; implemented as MCP server on CTFd platform
- **Dataset**: Dynamic (live competitions prevent data contamination)
- **Summary**: Live CTF evaluation framework that uses ongoing competitions with unreleased challenges to prevent data contamination and cheating via RAG/web search; MCP-based architecture.

---

### [VulnHub Pentest Benchmark](https://github.com/isamu-isozaki/AI-Pentest-Benchmark)
- **Category**: AI4Security > Offensive Capability > Penetration Testing
- **Created by**: Academic researchers
- **Used by**: Academic community
- **Scale**: 13 VulnHub boxes (7 easy, 4 medium, 2 hard) with verified walkthroughs
- **Dataset**: Open (VulnHub VMs are free)
- **Reference**: [Towards Automated Penetration Testing: Introducing LLM Benchmark, Analysis, and Improvements](https://arxiv.org/abs/2410.17141)
- **Summary**: End-to-end penetration testing benchmark using VulnHub VMs; evaluates LLMs on enumeration, exploitation, and privilege escalation phases.

---

### [SecLLMHolmes](https://github.com/ai4cloudops/SecLLMHolmes)
- **Category**: AI4Security > Offensive Capability > Vulnerability Detection
- **Created by**: Boston University, IBM Research
- **Used by**: Academic community
- **Scale**: 228 code scenarios evaluated across 8 investigative dimensions on 8 LLMs
- **Dataset**: Open
- **Reference**: [LLMs Cannot Reliably Identify and Reason About Security Vulnerabilities (Yet?)](https://arxiv.org/abs/2312.12575)
- **Summary**: Fully automated framework for evaluating LLM vulnerability detection and reasoning; shows LLMs provide non-deterministic, unfaithful reasoning and GPT-4 achieves only 13% accuracy on real-world file-level vulnerabilities.

---

### [VulDetectBench](https://github.com/Sweetaroo/VulDetectBench)
- **Category**: AI4Security > Offensive Capability > Vulnerability Detection
- **Created by**: Academic researchers
- **Used by**: Academic community
- **Scale**: 5 tasks of increasing difficulty covering 38-48 CWE types; 17 models evaluated
- **Dataset**: Open
- **Reference**: [VulDetectBench: Evaluating the Deep Capability of Vulnerability Detection with Large Language Models](https://arxiv.org/abs/2406.07595)
- **Summary**: Multi-task vulnerability detection benchmark (binary classification, CWE classification, root cause identification, trigger point localization); models achieve >80% on identification but <30% on detailed analysis.

---

### [PrimeVul](https://github.com/DLVulDet/PrimeVul)
- **Category**: AI4Security > Offensive Capability > Vulnerability Detection Dataset
- **Created by**: Academic researchers
- **Used by**: Google (Gemini 1.5 evaluation), academic community
- **Scale**: ~7,000 vulnerable functions + ~229,000 benign functions from real C/C++ projects; 140+ CWEs
- **Dataset**: Open
- **Reference**: [Vulnerability Detection with Code Language Models: How Far Are We?](https://arxiv.org/abs/2403.18624)
- **Summary**: High-accuracy vulnerability detection dataset with human-level labeling (3x more accurate than prior automatic methods); reveals existing benchmarks greatly overestimate model proficiency (StarCoder2: 68% on BigVul vs 3% on PrimeVul). ICSE 2025.

---

### [DiverseVul](https://github.com/wagner-group/diversevul)
- **Category**: AI4Security > Offensive Capability > Vulnerability Detection Dataset
- **Created by**: UC Berkeley (Wagner Group)
- **Used by**: Academic community
- **Scale**: 18,945 vulnerable functions + 330,492 non-vulnerable functions spanning 150 CWEs from 7,514 commits across 295+ projects
- **Dataset**: Open
- **Reference**: [DiverseVul: A New Vulnerable Source Code Dataset for Deep Learning Based Vulnerability Detection](https://dl.acm.org/doi/10.1145/3607199.3607242)
- **Summary**: Largest diverse vulnerability source code dataset covering 295 more projects than all prior datasets combined; shows LLMs outperform GNNs but best models still not deployment-ready (3.47% FPR, 47% F1). RAID 2023.

---

### [SWE-bench](https://github.com/SWE-bench/SWE-bench)
- **Category**: AI4Security > Offensive Capability > Software Engineering (security-adjacent)
- **Created by**: Princeton University
- **Used by**: OpenAI, Anthropic, Google (as general coding benchmark; cybersecurity-adjacent)
- **Scale**: 2,294 real GitHub issues from 12 Python repos; SWE-bench Verified: 500 human-validated subset
- **Dataset**: Open
- **Reference**: [SWE-bench: Can Language Models Resolve Real-world GitHub Issues?](https://arxiv.org/abs/2310.06770)
- **Summary**: Software engineering benchmark resolving real GitHub issues; security-relevant because LLM agents can introduce vulnerability classes (9x increase in some scenarios). SWE-agent variant explicitly supports offensive cybersecurity use. NeurIPS 2024.
