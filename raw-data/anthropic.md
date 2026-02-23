# Anthropic: Cybersecurity Evaluation Documentation

## Overview

- **Total Documents**: 24
- **Date Range**: 2023-07 ~ 2026-02
- **Risk Framework**: Responsible Scaling Policy (RSP v2.2) ([Web](https://www.anthropic.com/responsible-scaling-policy))
- **Backbone Models**: Claude Opus 4.6, Claude Sonnet 4.6, Claude Opus 4.5, Claude Sonnet 4.5, Claude Haiku 4.5, Claude Opus 4.1, Claude Opus 4, Claude Sonnet 4, Claude 3.7 Sonnet, Claude 3.5 Sonnet, Claude 3.5 Haiku, Claude 3 Opus, Claude 3 Sonnet, Claude 3 Haiku, Claude 2
- **Primary Benchmarks**: Cybench, CyberGym, CMU Cyber Ranges, Custom Network Challenges, Real CTF Competitions (PicoCTF, HackTheBox, WRCCDC)

---

## Frameworks

### 1. Responsible Scaling Policy (RSP) v1.0

- **Date**: 2023-09-19
- **URL**: [Web](https://www.anthropic.com/rsp-updates) | [PDF](https://www-cdn.anthropic.com/1adf000c8f675958c2ee23805d91aaade1cd4613/responsible-scaling-policy.pdf)
- **Models**: Framework for all Claude models
- **Type**: Framework
- **Cyber Risk Level**: Establishes ASL framework (ASL-1 through ASL-4)
- **Benchmarks Reported**: None (framework document)
- **Agent Setup**: N/A
- **Key Findings**: Establishes AI Safety Levels (ASL) framework; defines cybersecurity as one of three catastrophic risk domains (alongside CBRN and autonomous capabilities); sets ASL-3 cyber threshold: success >=1/5 times in >=2/6 classes of expert vulnerability discovery and exploit development evaluations
- **Notes**: Foundation document for all subsequent Anthropic cyber evaluations

### 2. RSP v2.2

- **Date**: 2025-05-14
- **URL**: [Web](https://www.anthropic.com/responsible-scaling-policy) | [PDF](https://www-cdn.anthropic.com/872c653b2d0501d6ab44cf87f43e1dc4853e4d37.pdf)
- **Models**: Framework for all models (triggered for Claude Opus 4)
- **Type**: Framework
- **Cyber Risk Level**: Updated ASL-3 thresholds
- **Benchmarks Reported**: None (framework document)
- **Agent Setup**: N/A
- **Key Findings**: Updated capability thresholds and security/deployment standards; triggered by Claude Opus 4 approaching ASL-3 thresholds

---

## Model Evaluations

### 3. Claude 2 Model Card

- **Date**: 2023-07
- **URL**: [Web](https://www.anthropic.com/claude-2-model-card) | [PDF](https://www-cdn.anthropic.com/bd2a28d2535bfb0494cc8e2a3bf135d2e7523226/Model-Card-Claude-2.pdf)
- **Models**: Claude 1.3, Claude 2
- **Type**: Model Card
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Red-teaming (crowd-worker) | Security4AI > Misuse Risk | Qualitative | Crowd-worker red teaming | Model Card |
  | National security risk eval | Security4AI > Misuse Risk | Qualitative | Expert evaluation | Model Card |
  | ARC safety audit | Security4AI > Alignment | Qualitative | Third-party audit | Model Card |
  | Harmful response testing | Security4AI > Misuse Risk | 328 prompts tested | Manual evaluation | Model Card |

- **Agent Setup**: No agentic setup; direct prompting
- **Key Findings**: No dedicated cybersecurity benchmarks (CTF etc.) at this stage; early safety evaluations focused on misuse potential
- **Notes**: Earliest Anthropic model card; cybersecurity not yet a dedicated evaluation domain

### 4. Claude 3 Model Card (Opus, Sonnet, Haiku)

- **Date**: 2024-03
- **URL**: [PDF](https://www-cdn.anthropic.com/c6a80a657af445f40e31afac050f3bf76d3b1404.pdf)
- **Models**: Claude 3 Haiku, Claude 3 Sonnet, Claude 3 Opus
- **Type**: Model Card
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | CTF challenges (pwn, RE, crypto, web) | AI4Security > Offensive Capability | Qualitative | Internal CTF evaluation | Model Card |

- **Agent Setup**: Basic tool-use for CTF challenges
- **Key Findings**: First Claude model family with dedicated CTF evaluation across multiple categories (pwn, reverse engineering, crypto, web)

### 5. Claude 3.5 Sonnet Model Card Addendum

- **Date**: 2024-06
- **URL**: [PDF](https://www-cdn.anthropic.com/fed9cc193a14b84131812372d8d5857f8f304c52/Model_Card_Claude_3_Addendum.pdf)
- **Models**: Claude 3.5 Sonnet (original)
- **Type**: Addendum
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | CTF (pwn, RE, crypto, web) | AI4Security > Offensive Capability | Qualitative | Internal CTF evaluation | Addendum |

- **Agent Setup**: Tool-augmented CTF solving
- **Key Findings**: Incremental improvement over Claude 3 in CTF tasks
- **Notes**: US/UK AISI later used Cybench for Joint Pre-Deployment Test of this model

### 6. Claude 3.5 Haiku / Upgraded 3.5 Sonnet Addendum

- **Date**: 2024-10
- **URL**: [PDF](https://www-cdn.anthropic.com/c7822cdc35ad788ec87e14b3a9d45010f1f86c38.pdf)
- **Models**: Claude 3.5 Haiku, Claude 3.5 Sonnet (upgraded)
- **Type**: Addendum
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | CTF-based evaluations | AI4Security > Offensive Capability | Qualitative | Internal CTF evaluation | Addendum |

- **Agent Setup**: Tool-augmented CTF solving
- **Key Findings**: Continued ASL-2 classification; no significant uplift in offensive cyber capabilities

### 7. Claude 3.7 Sonnet System Card

- **Date**: 2025-02
- **URL**: [Web](https://anthropic.com/claude-3-7-sonnet-system-card) | [PDF](https://www-cdn.anthropic.com/9ff93dfa8f445c932415d335c88852ef47f1201e.pdf)
- **Models**: Claude 3.7 Sonnet
- **Type**: System Card
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | 35.9% | pass@5, 40 professional CTF tasks | System Card |
  | Prompt injection evals | Security4AI > Model Robustness | Evaluated | Internal methodology | System Card |

- **Agent Setup**: Agentic CTF solver with tool access
- **Key Findings**: First quantitative Cybench score reported; ~7x improvement over previous frontier model (from ~5% one year earlier); still classified ASL-2
- **Notes**: Cybench created by Stanford University (40 professional-level CTF tasks from 4 competitions)

### 8. Claude Opus 4 & Sonnet 4 System Card

- **Date**: 2025-05
- **URL**: [Web](https://www.anthropic.com/claude-4-system-card) | [PDF](https://www-cdn.anthropic.com/07b2a3f9902ee19fe39a36ca638e5ae987bc64dd.pdf)
- **Models**: Claude Opus 4, Claude Sonnet 4
- **Type**: System Card
- **Cyber Risk Level**: ASL-3 (Claude Opus 4 — first ASL-3 model)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Custom CTF (easy) | AI4Security > Offensive Capability | Opus: 11/11, Sonnet: 10/11 | Internal custom challenges | System Card |
  | Custom CTF (medium) | AI4Security > Offensive Capability | Opus: 1/2, Sonnet: 1/2 | Internal custom challenges | System Card |
  | Custom CTF (hard) | AI4Security > Offensive Capability | Opus: 0/2, Sonnet: 0/2 | Internal custom challenges | System Card |
  | Cyber-harness network challenges | AI4Security > Offensive Capability | Evaluated | Network infiltration scenarios | System Card |

- **Agent Setup**: Agentic setup with network tools, custom cyber harness environment
- **Key Findings**: Claude Opus 4 is the first model to reach ASL-3, exceeding thresholds in cyber and CBRN; approximately 120-page system card
- **Notes**: Triggered RSP v2.2 deployment safeguards

### 9. Claude Opus 4.1 System Card Addendum

- **Date**: 2025-08
- **URL**: [Web](https://www.anthropic.com/claude-opus-4-1-system-card) | [PDF](https://www-cdn.anthropic.com/9fa30625273bafdf5af82c93719d7ca606485a16.pdf)
- **Models**: Claude Opus 4.1
- **Type**: Addendum
- **Cyber Risk Level**: ASL-3 (maintained)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | Evaluated | CTF tasks | Addendum |
  | Custom cyber challenges | AI4Security > Offensive Capability | Evaluated | Internal challenges | Addendum |

- **Agent Setup**: Agentic setup with cyber tools
- **Key Findings**: Maintains ASL-3 classification; incremental improvement over Opus 4
- **Notes**: Claude Sonnet 4.5 later reported to have higher single-attempt success rate than Opus 4.1 with ten attempts on Cybench

### 10. Claude Sonnet 4.5 System Card

- **Date**: 2025-09
- **URL**: [Web](https://www.anthropic.com/claude-sonnet-4-5-system-card) | [PDF](https://www-cdn.anthropic.com/963373e433e489a87a10c823c52a0a013e9172dd.pdf)
- **Models**: Claude Sonnet 4.5
- **Type**: System Card
- **Cyber Risk Level**: ASL-3
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | 76.5% pass@10; 60% pass@1 | pass@10 (40 tasks) and pass@1 | System Card |
  | Cybench by category (pass@1) | AI4Security > Offensive Capability | Web: 11/13, Crypto: 14/18, Pwn: 2/7, Rev: 5/6, Network: 3/5 | Category-level breakdown | Opus 4.6 System Card (progression chart) |
  | CyberGym (pass@1) | AI4Security > Offensive Capability | 29.8% pass@1 | pass@1, real-world CVE detection | Opus 4.6 System Card (cross-model comparison) |
  | CyberGym ($2 cost limit) | AI4Security > Offensive Capability | 28.9% SOTA | Real-world CVE detection, $2 cost cap | System Card |
  | CyberGym (30 trials) | AI4Security > Offensive Capability | 66.7% vuln reproduction | 30 trial attempts, no cost limit | System Card |
  | CyberGym (30 trials, new vulns) | AI4Security > Offensive Capability | 33%+ new vuln discovery; 5% single trial | 30 trial attempts (vs Sonnet 4 ~2% single trial) | System Card |
  | CyberGym (patch generation) | AI4Security > Defensive Capability | 15% semantic match | Generated patches vs reference patches | AI for Cyber Defenders |
  | CMU Cyber Ranges | AI4Security > Offensive Capability | Evaluated | ~50-host network simulations | System Card |
  | Equifax Simulation | AI4Security > Offensive Capability | 2/5 autonomous | 5 independent trial runs | System Card |
  | Malicious computer use | Security4AI > Misuse Risk | 86.08% refusal rate | Without mitigations | Opus 4.6 System Card |

- **Agent Setup**: Agentic setup with standard Kali Linux tools; operates on ~50-host network simulations; Equifax simulation used only publicly disclosed CVE exploitation
- **Key Findings**: Cybench pass@10 doubled from 3.7 Sonnet's 35.9% to 76.5%; Cybench pass@1 at 60%; CyberGym pass@1 at 29.8%; SOTA on CyberGym at $2 cost; first to demonstrate autonomous Equifax breach reproduction (2/5 trials); single-attempt success rate higher than Opus 4.1 with ten attempts; patch generation 15% semantic match with merged open-source patches
- **Notes**: CyberGym created by UC Berkeley RDI (1,507 known CVEs). CMU Cyber Ranges developed collaboratively with Carnegie Mellon University's CyLab and Incalmo. Cybench pass@1 (60%) and category breakdown sourced from Opus 4.6 system card progression chart. CyberGym pass@1 (29.8%) from Opus 4.6 system card cross-model comparison (slightly differs from 28.9% at $2 cost limit). Sonnet 4: novel vulns in ~2% of targets vs Sonnet 4.5: 5% single trial.

### 11. Claude Haiku 4.5 System Card

- **Date**: 2025-10
- **URL**: [Web](https://www.anthropic.com/claude-haiku-4-5-system-card) | [PDF](https://www-cdn.anthropic.com/7aad69bf12627d42234e01ee7c36305dc2f6a970.pdf)
- **Models**: Claude Haiku 4.5
- **Type**: System Card
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | RSP evaluations | Security4AI > Misuse Risk | 87.7% appropriate assistance | Legitimate security research prompts | System Card |
  | Malicious computer use | Security4AI > Misuse Risk | 77.68% refusal rate | Without mitigations | Opus 4.6 System Card |

- **Agent Setup**: Standard prompting
- **Key Findings**: Remains ASL-2; 87.7% appropriate assistance rate on legitimate security research queries; 77.68% malicious computer use refusal rate (lowest among 4.5+ family)

### 12. Claude Opus 4.5 System Card

- **Date**: 2025-11
- **URL**: [Web](https://www.anthropic.com/claude-opus-4-5-system-card) | [PDF](https://www-cdn.anthropic.com/bf10f64990cfda0ba858290be7b8cc6317685f47.pdf)
- **Models**: Claude Opus 4.5
- **Type**: System Card
- **Cyber Risk Level**: ASL-3
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | 82% pass@1 | pass@1, professional CTF tasks | System Card |
  | Cybench by category | AI4Security > Offensive Capability | Web: 12/13, Crypto: 15/18, Pwn: 3/7, Rev: 6/6, Network: 4/5 | Category-level breakdown | System Card |
  | CyberGym | AI4Security > Offensive Capability | 51.0% pass@1 | pass@1, real-world CVE detection | System Card |
  | Network challenges | AI4Security > Offensive Capability | First unassisted solve | Multi-host network infiltration | System Card |
  | Cyber-harness network challenges | AI4Security > Offensive Capability | Evaluated | Network scenarios | System Card |
  | Prompt injection (coding, extended thinking) | Security4AI > Model Robustness | 0.3% ASR at k=1; 10.0% at k=200 (no safeguards); 0.1% at k=1; 7.5% at k=200 (with safeguards) | Shade indirect PI in coding env | System Card |
  | Prompt injection (coding, standard thinking) | Security4AI > Model Robustness | 0.7% ASR at k=1; 17.5% at k=200 (no safeguards); 0.2% at k=1; 7.5% at k=200 (with safeguards) | Shade indirect PI in coding env | System Card |
  | Prompt injection (browser) | Security4AI > Model Robustness | 1.4% ASR at k=100 (with safeguards) | Browser-based evaluation | System Card |
  | Malicious computer use | Security4AI > Misuse Risk | 88.39% refusal rate | Without mitigations | System Card |

- **Agent Setup**: Agentic setup with network tools and cyber harness
- **Key Findings**: First successful network challenge solve without human assistance; 82% Cybench pass@1; 51.0% CyberGym pass@1; prompt injection in coding: 0.3% at k=1 (extended thinking) to 0.7% at k=1 (standard thinking)
- **Notes**: CyberGym pass@1 score also reported as 50.63% in some sources; 51.0% from cross-model comparison in Opus 4.6 system card. Cybench category breakdown from Opus 4.6 system card progression chart.

### 13. Claude Opus 4.6 System Card

- **Date**: 2026-02
- **URL**: [Web](https://anthropic.com/claude-opus-4-6-system-card) | [PDF](https://www-cdn.anthropic.com/0dd865075ad3132672ee0ab40b05a53f14cf5288.pdf)
- **Models**: Claude Opus 4.6
- **Type**: System Card
- **Cyber Risk Level**: ASL-3
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | 93% pass@1 (37 tasks); ~100% pass@30 (saturated) | pass@1 and pass@30, 37 professional CTF tasks | Section 8.4.7 (p202) |
  | Cybench by category | AI4Security > Offensive Capability | Web: 13/13, Crypto: 16/18, Pwn: 5/7, Rev: 6/6, Network: 5/5 | Category-level breakdown | Section 8.4.7 (p202) |
  | CyberGym | AI4Security > Offensive Capability | 66.6% pass@1 (1,507 CVEs) | pass@1, real-world CVE detection, no thinking, default effort | Section 2.17 (p28-29) |
  | RSP Cyber CTF — Web | AI4Security > Offensive Capability | 13/13 | 15 challenges (11 easy, 2 med, 2 hard); Easy 8/8, Med 4/4, Hard 1/1 | Section 8.4.2 (p198) |
  | RSP Cyber CTF — Crypto | AI4Security > Offensive Capability | 16/18 | 22 challenges (7 easy, 6 med, 9 hard); Easy 5/5, Med 8/8, Hard 3/5 | Section 8.4.3 (p198) |
  | RSP Cyber CTF — Pwn | AI4Security > Offensive Capability | 5/7 | 9 challenges (5 easy, 2 med, 2 hard); Easy 2/2, Med 2/3, Hard 1/1, Expert 0/1 | Section 8.4.4 (p199) |
  | RSP Cyber CTF — Rev | AI4Security > Offensive Capability | 6/6 | 8 challenges (5 easy, 2 med, 1 hard); Easy 3/3, Med 1/1, Hard 2/2 | Section 8.4.5 (p200) |
  | RSP Cyber CTF — Network | AI4Security > Offensive Capability | 5/5 | 4 challenges (1 easy, 3 med); Easy 1/1, Med 3/3, Hard 1/1 | Section 8.4.6 (p201) |
  | Aggregate Cyber by Category (pass@30) | AI4Security > Offensive Capability | PWN ~71%, WEB 100%, CRYPTO ~94%, REV 100%, NETWORK 100%, MISC 100%, FORENSICS 100% | Aggregate success rates across all CTF challenges | Section 8.4.6.B (p201) |
  | 40 Cybersecurity Investigations | AI4Security > Defensive Capability | 38/40 blind-ranked best | Blind-ranked vs Claude 4.5 models, up to 9 subagents, 100+ tool calls | System Card |
  | Zero-day Discovery | Security4AI > Misuse Risk | 500+ zero-days | Pre-release testing, validated by internal team and external researchers | System Card |
  | CAISI Assessment | AI4Security > Offensive Capability | Novel vulns discovered in open & closed source software | US Center for AI Standards and Innovation, 1-week evaluation, hundreds of challenges | Section 8.4.8 (p202) |
  | 6 new cybersecurity probes | Security4AI > Misuse Risk | Evaluated | New probe evaluations for tracking misuse | System Card |
  | Agent Red Teaming (ART) benchmark | Security4AI > Model Robustness | k=1: 0.2%, k=10: 2.1%, k=100: 14.8% (no thinking); k=1: 0.2%, k=10: 2.2%, k=100: 21.7% (with thinking) | Gray Swan / UK AISI, 19 scenarios, indirect PI only | Section 5.2.1 (p84) |
  | Prompt injection (coding, extended thinking) | Security4AI > Model Robustness | 0.0% ASR at k=1; 0.0% ASR at k=200 (no safeguards); 0.0% at k=1; 0.0% at k=200 (with safeguards) | Shade indirect PI in coding env | Section 5.2.2.1 (p85) |
  | Prompt injection (coding, standard thinking) | Security4AI > Model Robustness | 0.0% ASR at k=1; 0.0% ASR at k=200 (no safeguards); 0.0% at k=1; 0.0% at k=200 (with safeguards) | Shade indirect PI in coding env | Section 5.2.2.1 (p85) |
  | Prompt injection (computer use, extended thinking) | Security4AI > Model Robustness | 17.8% ASR at k=1; 78.6% at k=200 (no safeguards); 9.7% at k=1; 57.1% at k=200 (with safeguards) | Shade indirect PI in computer use env (stronger attacker variant) | Section 5.2.2.2 (p86) |
  | Prompt injection (computer use, standard thinking) | Security4AI > Model Robustness | 20.0% ASR at k=1; 85.7% at k=200 (no safeguards); 10.0% at k=1; 64.3% at k=200 (with safeguards) | Shade indirect PI in computer use env (stronger attacker variant) | Section 5.2.2.2 (p86) |
  | Prompt injection (browser, Best-of-N, without safeguards) | Security4AI > Model Robustness | Ext: 2.06%/0.29%; Std: 2.83%/0.49% (scenario/attempt ASR) | Internal Best-of-N PI, 389 scenarios, 10 attacks each | Section 5.2.2.3 (p88) |
  | Prompt injection (browser, Best-of-N, with previous safeguards) | Security4AI > Model Robustness | 0.26%/0.03% (scenario/attempt ASR, standard thinking) | Internal Best-of-N PI with previous safeguards | Section 5.2.2.3 (p88) |
  | Prompt injection (browser, Best-of-N, with updated safeguards) | Security4AI > Model Robustness | 0.77%/0.08% (scenario/attempt ASR, standard thinking) | Internal Best-of-N PI with updated safeguards | Section 5.2.2.3 (p88) |
  | Malicious computer use | Security4AI > Misuse Risk | 88.34% refusal rate | Without mitigations | Section 5.1.3 |
  | Malicious Claude Code use (without mitigations) | Security4AI > Misuse Risk | 83.20% malicious refusal; 91.75% dual-use/benign success | Claude Code tools | Section 5.1.2 |
  | Malicious Claude Code use (with mitigations) | Security4AI > Misuse Risk | 99.59% malicious refusal; 95.59% dual-use/benign success | Claude Code tools with prompting mitigations | Section 5.1.2 |

- **Agent Setup**: Full agentic setup with network tools, vulnerability scanning, and investigation capabilities; Kali-based environment with pwntools, metasploit, ghidra, tshark; code editor + Terminal Tool with async terminal management; reports pass@30 trials
- **Key Findings**: Cybench 93% pass@1 (highest reported for any model); saturated Cybench at ~100% pass@30; CyberGym 66.6% pass@1 (highest reported); best in 38/40 blind-ranked cybersecurity investigations vs Claude 4.5 models; 500+ zero-day vulnerabilities discovered in pre-release testing; 0% prompt injection success in coding environments (all configurations); CAISI assessment discovered novel vulnerabilities in both open and closed source software; Opus 4.6 without extended thinking achieves ART robustness comparable to Opus 4.5 (14.8% vs 16.5% at k=100); unusually, extended thinking increases ART attack success (21.7% vs 14.8% at k=100) -- opposite of prior models; 212-page system card
- **Notes**: Cybench saturated -- Anthropic states current benchmarks can no longer track capability progression. CyberGym run with no thinking, default effort, temperature, and top_p, with a "think" tool for interleaved thinking. Computer use PI uses stronger attacker variant (previous version saturated at 0% for Opus 4.5 with extended thinking). Browser PI data from Opus 4.6 system card (Tables 5.2.2.3.A and 5.2.2.3.B). ART benchmark numbers updated with corrected grading (may differ from previous system cards). CAISI: US Center for AI Standards and Innovation assessed cyber capabilities over one-week window in partnership with US Government.

### 14. Claude Sonnet 4.6 System Card

- **Date**: 2026-02-17
- **URL**: [Web](https://anthropic.com/claude-sonnet-4-6-system-card) | [PDF](https://www-cdn.anthropic.com/78073f739564e986ff3e28522761a7a0b4484f84.pdf)
- **Models**: Claude Sonnet 4.6
- **Type**: System Card
- **Cyber Risk Level**: ASL-3
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | 90% pass@1 (37 tasks); 100% pass@30 (saturated) | pass@1 and pass@30, 37 professional CTF tasks (3 excluded due to infra/timing) | System Card Section 6.4.7 |
  | RSP Cyber CTF — Web | AI4Security > Offensive Capability | 13/13 | 15 challenges (11 easy, 2 med, 2 hard); solved 13 | System Card Section 6.4.2 |
  | RSP Cyber CTF — Crypto | AI4Security > Offensive Capability | 16/18 | 22 challenges (7 easy, 6 med, 9 hard); solved 16 | System Card Section 6.4.3 |
  | RSP Cyber CTF — Pwn | AI4Security > Offensive Capability | 5/7 | 9 challenges (5 easy, 2 med, 2 hard); solved 5 | System Card Section 6.4.4 |
  | RSP Cyber CTF — Rev | AI4Security > Offensive Capability | 6/6 | 8 challenges (5 easy, 2 med, 1 hard); solved 6 | System Card Section 6.4.5 |
  | RSP Cyber CTF — Network | AI4Security > Offensive Capability | 5/5 | 4 challenges (1 easy, 3 med); solved all + extra | System Card Section 6.4.6 |
  | CyberGym | AI4Security > Offensive Capability | 65.2% pass@1 | pass@1, real-world CVE detection | System Card |
  | Prompt injection (coding, extended thinking) | Security4AI > Model Robustness | 0.0% ASR at k=1; 0.0% at k=200 (no safeguards); 0.0% at k=1; 0.0% at k=200 (with safeguards) | Shade indirect PI in coding env | System Card Section 5.2.2.1 |
  | Prompt injection (coding, standard thinking) | Security4AI > Model Robustness | 0.1% ASR at k=1; 7.5% at k=200 (no safeguards); 0.04% at k=1; 5.0% at k=200 (with safeguards) | Shade indirect PI in coding env | System Card Section 5.2.2.1 |
  | Prompt injection (computer use, extended thinking) | Security4AI > Model Robustness | 12.0% ASR at k=1; 42.9% at k=200 (no safeguards); 8.0% at k=1; 50.0% at k=200 (with safeguards) | Shade indirect PI in computer use env | System Card Section 5.2.2.2 |
  | Prompt injection (computer use, standard thinking) | Security4AI > Model Robustness | 14.4% ASR at k=1; 64.3% at k=200 (no safeguards); 8.6% at k=1; 50.0% at k=200 (with safeguards) | Shade indirect PI in computer use env | System Card Section 5.2.2.2 |
  | Prompt injection (browser, Best-of-N, without safeguards) | Security4AI > Model Robustness | Ext: 1.29%/0.24%; Std: 1.29%/0.29% (scenario/attempt ASR) | Internal Best-of-N PI, 389 scenarios, 10 attacks each | System Card Section 5.2.2.3 |
  | Prompt injection (browser, Best-of-N, with previous safeguards) | Security4AI > Model Robustness | 1.03%/0.16% (scenario/attempt ASR, standard thinking) | Internal Best-of-N PI with previous safeguards | System Card Section 5.2.2.3 |
  | Prompt injection (browser, Best-of-N, with updated safeguards) | Security4AI > Model Robustness | 0.51%/0.08% (scenario/attempt ASR, standard thinking) | Internal Best-of-N PI with updated safeguards | System Card Section 5.2.2.3 |
  | Agent Red Teaming (ART) benchmark | Security4AI > Model Robustness | k=1: 2.20%, k=10: 15.94%, k=100: 20.72% (no thinking); k=1: 2.73% (with thinking) | Gray Swan / UK AISI, 19 scenarios, indirect PI only, updated grading | System Card Section 5.2.1 (Figure 5.2.1.A) |
  | Agentic coding refusal | Security4AI > Misuse Risk | 100% refusal rate | 150 malicious coding requests, without mitigations | System Card Section 5.1.1 |
  | Malicious Claude Code use (without mitigations) | Security4AI > Misuse Risk | 79.34% malicious refusal; 88.52% dual-use/benign success | Claude Code tools | System Card Section 5.1.2 |
  | Malicious Claude Code use (with mitigations) | Security4AI > Misuse Risk | 99.39% malicious refusal; 91.78% dual-use/benign success | Claude Code tools with prompting mitigations | System Card Section 5.1.2 |
  | Malicious computer use | Security4AI > Misuse Risk | 99.38% refusal rate | 112 tasks, extended + standard thinking (224 attempts), without mitigations | System Card Section 5.1.3 |

- **Agent Setup**: Evaluated in coding, computer use, and browser environments with extended and standard thinking
- **Key Findings**: ASL-3 (first Sonnet-class model deployed under ASL-3 Standard); Cybench 90% pass@1 (37 tasks), just below Opus 4.6 (93%); saturated at 100% pass@30; CyberGym 65.2% pass@1 -- nearly matches Opus 4.6 (66.6%), more than doubled from Sonnet 4.5 (29.8%); near-perfect prompt injection resistance: 0% in coding with extended thinking, <0.3% in browser environments; first Sonnet-class model to achieve Opus-level prompt injection resistance; major improvement over Sonnet 4.5 in computer use PI defense; 99.38% malicious computer use refusal (highest among all Claude models); 100% agentic coding refusal rate; Shade computer use PI ASR substantially lower than Opus 4.6 (12.0% vs 17.8% ext thinking, no safeguards); ART benchmark k=1: 2.20% comparable to Opus 4.6 (0.2%)
- **Notes**: ASL-3 (deployed under ASL-3 Standard, same as Opus 4.6). Matches Opus 4.6 prompt injection resistance in coding -- significant for enterprise deployment at Sonnet-tier pricing. Computer use PI: Sonnet 4.6 actually outperforms Opus 4.6 (lower ASR). ART benchmark: k=1 2.20% / k=10 15.94% / k=100 20.72% (no thinking), k=1 2.73% (thinking) -- comparable to Opus 4.6 and major improvement over Sonnet 4.5 (k=1: 9.31%/10.85%). Browser Best-of-N: with updated safeguards, 0.51%/0.08% scenario/attempt ASR -- competitive with Opus 4.6 (0.77%/0.08%).

---

## Red Team / External Reports

### 15. Frontier Threats Red Teaming for AI Safety

- **Date**: 2023-07
- **URL**: [Web](https://www.anthropic.com/news/frontier-threats-red-teaming-for-ai-safety)
- **Models**: Pre-Claude 2 snapshots, Claude 2
- **Type**: Report
- **Cyber Risk Level**: N/A (methodology paper)
- **Benchmarks Reported**: None (qualitative dual-use assessment)
- **Agent Setup**: Direct prompting for dual-use capability assessment
- **Key Findings**: Biosecurity-focused but establishes methodology for dual-use capability assessment applicable to cybersecurity domain

### 16. ASL-3 Deployment Safeguards Report

- **Date**: 2025-05
- **URL**: [Web](https://www.anthropic.com/asl3-deployment-safeguards)
- **Models**: Claude Opus 4
- **Type**: Report
- **Cyber Risk Level**: ASL-3 safeguards
- **Benchmarks Reported**: None (safeguards report)
- **Agent Setup**: N/A
- **Key Findings**: Details threat modeling, defense-in-depth measures, universal jailbreak resistance, and access controls for ASL-3 deployment

### 17. Activating ASL-3 Protections Report

- **Date**: 2025-05
- **URL**: [Web](https://www.anthropic.com/activating-asl3-report)
- **Models**: Claude Opus 4
- **Type**: Report
- **Cyber Risk Level**: ASL-3 threshold evidence
- **Benchmarks Reported**: None (threshold assessment)
- **Agent Setup**: N/A
- **Key Findings**: Provides evidence that Claude Opus 4 exceeds ASL-3 thresholds in both cyber and CBRN domains

### 18. Cyber Competitions (Frontier Red Team)

- **Date**: 2025
- **URL**: [Web](https://red.anthropic.com/2025/cyber-competitions/)
- **Models**: Claude (model versions not specified per competition)
- **Type**: Report
- **Cyber Risk Level**: N/A (capability evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | PicoCTF 2025 | AI4Security > Offensive Capability | 297th/10,460 (top 3%), 32/41 challenges | Live competition, Mar 7-17 | Cyber Competitions |
  | HackTheBox AI vs Human | AI4Security > Offensive Capability | 30th/161 overall, 4th/8 AI teams, 19/20 challenges | Live competition, Mar 14-16 | Cyber Competitions |
  | WRCCDC Regional | AI4Security > Defensive Capability | 6th/9 teams | Live defensive competition, Mar 28 | Cyber Competitions |
  | WRCCDC Qualifier | AI4Security > Defensive Capability | 10th/28 teams | 8-hour defensive competition, Feb 8 | Cyber Competitions |
  | PlaidCTF | AI4Security > Offensive Capability | 0 challenges solved | Advanced difficulty, Apr 4 | Cyber Competitions |
  | DEF CON CTF Qualifier | AI4Security > Offensive Capability | 0 challenges solved | Elite difficulty, Apr 12-14 | Cyber Competitions |
  | Airbnb Competition | AI4Security > Offensive Capability | 39th/~180 teams, 15/30 challenges | Live competition, Jun 24-26 | Cyber Competitions |

- **Agent Setup**: Autonomous Claude agent competing in real-world CTF events
- **Key Findings**: Strong performance at intermediate level (PicoCTF top 3%, HTB 19/20); unable to solve any advanced-difficulty challenges (PlaidCTF, DEF CON); defensive competitions competitive with college-level teams
- **Notes**: HTB note: if Claude had started on time (32 min late), would have placed 22nd overall and 1st among AI teams

### 19. AI for Cyber Defenders (Frontier Red Team)

- **Date**: 2025
- **URL**: [Web](https://red.anthropic.com/2025/ai-for-cyber-defenders/)
- **Models**: Claude Sonnet 4, Claude Sonnet 4.5
- **Type**: Report
- **Cyber Risk Level**: N/A (capability evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | CyberGym (Sonnet 4) | AI4Security > Offensive Capability | Strongest on public leaderboard; ~2% novel vuln discovery (single trial) | Public leaderboard ranking | AI for Cyber Defenders |
  | CyberGym ($2 cost, Sonnet 4.5) | AI4Security > Offensive Capability | 28.9% SOTA | $2 cost limit per challenge | AI for Cyber Defenders |
  | CyberGym (30 trials, Sonnet 4.5) | AI4Security > Offensive Capability | 66.7% vuln reproduction | 30 trial attempts | AI for Cyber Defenders |
  | CyberGym (30 trials, new vulns, Sonnet 4.5) | AI4Security > Offensive Capability | 33%+ new vuln discovery; 5% single trial | 30 trial attempts (~$45/task) | AI for Cyber Defenders |
  | CyberGym (patch generation, Sonnet 4.5) | AI4Security > Defensive Capability | 15% semantic match | Patches vs reference patches for merged PRs | AI for Cyber Defenders |
  | Cybench (Sonnet 4.5) | AI4Security > Offensive Capability | 76.5% pass@10; 2x from Sonnet 3.7 | pass@10, 40 tasks | AI for Cyber Defenders |
  | Cybench time comparison | AI4Security > Offensive Capability | 38 min (Claude) vs 60+ min (human est.) | Example malware analysis challenge | AI for Cyber Defenders |

- **Agent Setup**: Automated vulnerability detection agent against real open-source codebases
- **Key Findings**: Claude Sonnet 4 strongest on CyberGym public leaderboard (~2% novel vuln single trial); Sonnet 4.5 achieved SOTA 28.9% at $2 cost; 66.7% vulnerability reproduction rate; 33%+ previously unknown vulnerability discovery (5% single trial); 15% patch generation semantic match; Cybench doubled from 35.9% to 76.5% within 6 months; Claude solved example challenge in 38 min vs human estimate of 60+ min
- **Notes**: CyberGym created by UC Berkeley RDI, NOT Anthropic. Contains 1,507 known CVEs. Patch generation: 15% of Claude-generated patches matched reference patches semantically; manual analysis confirmed functional equivalence with merged open-source patches.

### 20. Progress from Frontier Red Team

- **Date**: 2025
- **URL**: [Web](https://www.anthropic.com/news/strategic-warning-for-ai-risk-progress-and-insights-from-our-frontier-red-team)
- **Models**: Multiple Claude models (longitudinal analysis)
- **Type**: Report
- **Cyber Risk Level**: N/A (longitudinal assessment)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | InterCode CTF | AI4Security > Offensive Capability | <25% to ~100% (over 1 year) | High school-level CTF challenges | Report |
  | Cybench | AI4Security > Offensive Capability | ~5% to 35.9% (over 1 year) | Professional-level CTF tasks | Report |

- **Agent Setup**: Agentic setup with varying tool access; tested both autonomous and tool-assisted (Incalmo)
- **Key Findings**: Models improved from "high schooler to undergraduate level" in one year; still cannot autonomously succeed on realistic 50-host cyber ranges requiring multi-stage attacks; tool augmentation (Incalmo) significantly enhances capabilities; models fall short of national security risk thresholds

### 21. Framework for Evaluating Emerging Cyberattack Capabilities

- **Date**: 2025-03-14
- **URL**: [arXiv](https://arxiv.org/abs/2503.11917)
- **Models**: Frontier AI models including Claude
- **Type**: Paper
- **Cyber Risk Level**: N/A (methodology paper)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | End-to-end attack chain framework | AI4Security > Offensive Capability | 50 new challenges | 12,000+ real-world AI-in-cyber incidents | Paper |

- **Agent Setup**: End-to-end attack chain evaluation
- **Key Findings**: Proposes framework based on 12,000+ real-world AI-in-cyber incidents; introduces 50 new evaluation challenges

### 22. Pilot Sabotage Risk Report

- **Date**: 2025 (Summer)
- **URL**: [Web](https://alignment.anthropic.com/2025/sabotage-risk-report/) | [PDF](https://alignment.anthropic.com/2025/sabotage-risk-report/2025_pilot_risk_report.pdf)
- **Models**: Claude Opus 4
- **Type**: Report
- **Cyber Risk Level**: ASL-3 (alignment risk assessment)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Sabotage risk evaluation | Security4AI > Alignment | 9 pathways assessed | Expert review by METR | Report |

- **Agent Setup**: Agentic Claude Opus 4 evaluated for sabotage behaviors
- **Key Findings**: Identifies 9 sabotage risk pathways for agentic AI systems; reviewed by METR (third-party evaluator)

### 23. Threat Intelligence Report: AI-Orchestrated Cyber Espionage

- **Date**: 2025-08
- **URL**: [Web](https://www.anthropic.com/news/disrupting-AI-espionage) | [PDF](https://assets.anthropic.com/m/ec212e6566a0d47/original/Disrupting-the-first-reported-AI-orchestrated-cyber-espionage-campaign.pdf)
- **Models**: Claude (adversary use in the wild)
- **Type**: Report
- **Cyber Risk Level**: Real-world adversary use documentation
- **Benchmarks Reported**: None (incident report)
- **Agent Setup**: Adversary used Claude via Claude Code for automated cyber operations
- **Key Findings**: First documented AI-orchestrated cyber espionage campaign; Chinese state-sponsored actor (GTG-1002) used Claude for espionage operations; data extortion campaigns targeting 17+ organizations via Claude Code; North Korean actors also identified using Claude for fraud schemes

### 24. AI Models on Realistic Cyber Ranges (Frontier Red Team)

- **Date**: 2026-01-16
- **URL**: [Web](https://red.anthropic.com/2026/cyber-toolkits-update/)
- **Models**: Claude Sonnet 4.5
- **Type**: Report
- **Cyber Risk Level**: N/A (capability evaluation)
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Equifax Simulation | AI4Security > Offensive Capability | 2/5 autonomous | 5 autonomous trial runs | Report |
  | Network simulations | AI4Security > Offensive Capability | 9 networks tested, toolkit needed for 5 | Multi-host network scenarios | Report |
  | CVE recognition | AI4Security > Offensive Capability | Instant recognition | Publicly disclosed CVE exploitation | Report |

- **Agent Setup**: Claude Sonnet 4.5 with standard Kali Linux tools; tested both with and without custom cyber toolkit (Incalmo) on CMU CyLab-developed ranges
- **Key Findings**: Autonomous Equifax breach reproduction in 2/5 trials using only standard tools; can succeed on minority of networks without custom cyber toolkit; instant CVE recognition without iterative refinement; previous version (Sonnet 3.5) failed all 5 trials without toolkit

---

## Cybench Performance Progression

| Model | Date | Cybench Score | Methodology | Source |
|---|---|---|---|---|
| Claude 3.7 Sonnet | 2025-02 | 35.9% | pass@5, 40 tasks | [System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
| Claude Sonnet 4.5 | 2025-09 | 76.5% (pass@10); 60% (pass@1) | pass@10 and pass@1, 40 tasks | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.5 | 2025-11 | 82% (pass@1, full 40 tasks); 79% (pass@1, RSP 37-task subset) | pass@1 | [System Card](https://www.anthropic.com/claude-opus-4-5-system-card); Opus 4.6 SC Fig 8.4.7 |
| Claude Sonnet 4.6 | 2026-02 | 90% (pass@1); 100% (pass@30, saturated) | pass@1 and pass@30, 37 tasks | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | 2026-02 | 93% (pass@1); ~100% (pass@30, saturated) | pass@1 and pass@30, 37 tasks | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

### Cybench Category Breakdown (pass@1)

| Category | Sonnet 4.5 | Opus 4.5 | Sonnet 4.6 | Opus 4.6 |
|---|---|---|---|---|
| Web | 11/13 | 12/13 | 13/13 | 13/13 |
| Crypto | 14/18 | 15/18 | 16/18 | 16/18 |
| Pwn | 2/7 | 3/7 | 5/7 | 5/7 |
| Rev | 5/6 | 6/6 | 6/6 | 6/6 |
| Network | 3/5 | 4/5 | 5/5 | 5/5 |
| **Total** | **~60%** | **~79%** | **~90%** | **~93%** |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) progression chart; [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Sections 6.4.2-6.4.7. Note: Category totals (13+18+7+6+5=49 tasks) differ from original Cybench's 40-task count, suggesting expanded or sub-task-level evaluation. Sonnet 4.6 matches Opus 4.6 in every category. The ~60%/~79%/~90%/~93% progression figures are from the system cards' own reporting and may use different weighting than raw category sums.

---

## CyberGym Performance Progression

| Model | Date | CyberGym pass@1 | Source |
|---|---|---|---|
| Claude Sonnet 4 | 2025-05 | Strongest on public leaderboard (exact % N/A) | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | 2025-09 | 29.8% (also 28.9% at $2 cost limit) | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.5 | 2025-11 | 51.0% | [System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Sonnet 4.6 | 2026-02 | 65.2% | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | 2026-02 | 66.6% | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) cross-model comparison; [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) for Sonnet 4.6

---

## Prompt Injection Resistance (Shade Indirect PI in Coding Environments)

| Model | Thinking Mode | ASR k=1 (no safeguards) | ASR k=200 (no safeguards) | ASR k=1 (with safeguards) | ASR k=200 (with safeguards) |
|---|---|---|---|---|---|
| Claude Sonnet 4.6 | Extended | 0.0% | 0.0% | 0.0% | 0.0% |
| Claude Sonnet 4.6 | Standard | 0.1% | 7.5% | 0.04% | 5.0% |
| Claude Opus 4.6 | Extended | 0.0% | 0.0% | 0.0% | 0.0% |
| Claude Opus 4.6 | Standard | 0.0% | 0.0% | 0.0% | 0.0% |
| Claude Opus 4.5 | Extended | 0.3% | 10.0% | 0.1% | 7.5% |
| Claude Opus 4.5 | Standard | 0.7% | 17.5% | 0.2% | 7.5% |
| Claude Sonnet 4.5 | Extended | 18.3% | 70.0% | 1.6% | 25.0% |
| Claude Sonnet 4.5 | Standard | 31.6% | 87.5% | 1.7% | 25.0% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) (Table 5.2.2.1.A); originally from [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) for Opus models

---

## Prompt Injection Resistance (Shade Indirect PI in Computer Use Environments)

| Model | Thinking Mode | ASR k=1 (no safeguards) | ASR k=200 (no safeguards) | ASR k=1 (with safeguards) | ASR k=200 (with safeguards) |
|---|---|---|---|---|---|
| Claude Sonnet 4.6 | Extended | 12.0% | 42.9% | 8.0% | 50.0% |
| Claude Sonnet 4.6 | Standard | 14.4% | 64.3% | 8.6% | 50.0% |
| Claude Opus 4.6 | Extended | 17.8% | 78.6% | 9.7% | 57.1% |
| Claude Opus 4.6 | Standard | 20.0% | 85.7% | 10.0% | 64.3% |
| Claude Opus 4.5 | Extended | 28.0% | 78.6% | 17.3% | 64.3% |
| Claude Opus 4.5 | Standard | 35.4% | 85.7% | 18.8% | 71.4% |
| Claude Sonnet 4.5 | Extended | 41.8% | 92.9% | 25.2% | 85.7% |
| Claude Sonnet 4.5 | Standard | 19.0% | 92.9% | 12.8% | 71.4% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) (Table 5.2.2.2.A)

---

## Prompt Injection Resistance (Best-of-N PI in Browser Use Environments)

### Without Safeguards

| Model | Thinking Mode | ASR % of Scenarios | ASR % of Attempts |
|---|---|---|---|
| Claude Sonnet 4.6 | Extended | 1.29% | 0.24% |
| Claude Sonnet 4.6 | Standard | 1.29% | 0.29% |
| Claude Opus 4.6 | Extended | 2.06% | 0.29% |
| Claude Opus 4.6 | Standard | 2.83% | 0.49% |
| Claude Opus 4.5 | Extended | 18.77% | 6.40% |
| Claude Opus 4.5 | Standard | 16.20% | 5.06% |
| Claude Sonnet 4.5 | Extended | 54.24% | 20.45% |
| Claude Sonnet 4.5 | Standard | 49.36% | 16.23% |

### With Safeguards (Standard Thinking)

| Model | Previous Safeguards (Scenarios) | Previous Safeguards (Attempts) | Updated Safeguards (Scenarios) | Updated Safeguards (Attempts) |
|---|---|---|---|---|
| Claude Sonnet 4.6 | 1.03% | 0.16% | 0.51% | 0.08% |
| Claude Opus 4.6 | 0.26% | 0.03% | 0.77% | 0.08% |
| Claude Opus 4.5 | 1.03% | 0.21% | 1.54% | 0.40% |
| Claude Sonnet 4.5 | 1.54% | 0.41% | 2.06% | 0.46% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) (Tables 5.2.2.3.A and 5.2.2.3.B). 389 scenarios, 10 attack strings each.

---

## Malicious Computer Use Refusal Rates (Without Mitigations)

| Model | Refusal Rate |
|---|---|
| Claude Sonnet 4.6 | 99.38% |
| Claude Opus 4.6 | 88.34% |
| Claude Opus 4.5 | 88.39% |
| Claude Sonnet 4.5 | 86.08% |
| Claude Haiku 4.5 | 77.68% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) (Table 5.1.3.A); [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) for earlier models

---

## Agentic Coding Refusal Rates (Without Mitigations)

| Model | Refusal Rate |
|---|---|
| Claude Sonnet 4.6 | 100% |
| Claude Opus 4.5 | 100% |
| Claude Haiku 4.5 | 100% |
| Claude Opus 4.6 | 99.3% |
| Claude Sonnet 4.5 | 98.7% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) (Table 5.1.1.A). 150 malicious coding requests.

---

## Malicious Claude Code Use

### Without Mitigations

| Model | Malicious Refusal Rate | Dual-use & Benign Success Rate |
|---|---|---|
| Claude Opus 4.6 | 83.20% | 91.75% |
| Claude Sonnet 4.6 | 79.34% | 88.52% |
| Claude Opus 4.5 | 77.80% | 93.07% |
| Claude Haiku 4.5 | 69.39% | 84.92% |
| Claude Sonnet 4.5 | 63.06% | 96.56% |

### With Mitigations

| Model | Malicious Refusal Rate | Dual-use & Benign Success Rate |
|---|---|---|
| Claude Opus 4.6 | 99.59% | 95.59% |
| Claude Sonnet 4.6 | 99.39% | 91.78% |
| Claude Opus 4.5 | 97.35% | 96.52% |
| Claude Haiku 4.5 | 96.73% | 86.07% |
| Claude Sonnet 4.5 | 95.10% | 98.20% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) (Tables 5.1.2.A and 5.1.2.B)

---

## Agent Red Teaming (ART) Benchmark — Indirect Prompt Injection Robustness

| Model | k=1 | k=10 | k=100 |
|---|---|---|---|
| Gemini 3 Flash | 17.8% | 63.6% | 73.3% |
| Gemini 3 Flash Thinking | 12.0% | 50.9% | 84.1% |
| Gemini 3 Pro | 7.1% | 40.0% | 74.2% |
| Gemini 3 Pro Preview | 7.0% | 39.6% | 75.6% |
| Gemini 3 Pro Thinking | 3.2% | 23.3% | 62.7% |
| GPT-5.2 | 2.3% | 16.6% | 49.2% |
| GPT-5.2 Thinking | 2.6% | 23.1% | 52.3% |
| Haiku 4.5 | 10.8% | 19.2% | 40.7% |
| Haiku 4.5 Thinking | 9.3% | 34.9% | — |
| Sonnet 4.5 | 1.1% | 9.31% | 34.9% |
| Sonnet 4.5 Thinking | 1.3% | 10.85% | 40.7% |
| Opus 4.5 | 2.0% | 16.5% | — |
| Opus 4.5 Thinking | 1.6% | 14.2% | — |
| Opus 4.6 | 0.2% | 2.1% | 14.8% |
| Opus 4.6 Thinking | 0.2% | 2.2% | 21.7% |
| Sonnet 4.6 | 2.2% | 15.9% | 20.7% |
| Sonnet 4.6 Thinking | 2.7% | — | — |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) Figure 5.2.1.A and [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Figure 5.2.1.A. Lower is better. Attack success evaluated on 19 scenarios. Numbers reflect updated grading (corrected in collaboration with Gray Swan; may differ from previous system cards). Some k=100 values not readable from figures marked with —.

---

## RSP Cyber CTF Per-Category Breakdown by Difficulty (pass@30)

### Web (15 challenges: 11 easy, 2 medium, 2 hard)

| Model | Easy | Medium | Hard | Total |
|---|---|---|---|---|
| Sonnet 4.5 | 8/8 | 2/4 | 1/1 | 11/13 |
| Opus 4.5 | 8/8 | 3/4 | 1/1 | 12/13 |
| Opus 4.6 | 8/8 | 4/4 | 1/1 | 13/13 |
| Sonnet 4.6 | 8/8 | 4/4 | 1/1 | 13/13 |

### Crypto (22 challenges: 7 easy, 6 medium, 9 hard)

| Model | Easy | Medium | Hard | Total |
|---|---|---|---|---|
| Sonnet 4.5 | 5/5 | 6/8 | 3/5 | 14/18 |
| Opus 4.5 | 5/5 | 6/8 | 4/5 | 15/18 |
| Opus 4.6 | 5/5 | 8/8 | 3/5 | 16/18 |
| Sonnet 4.6 | 5/5 | 8/8 | 3/5 | 16/18 |

### Pwn (9 challenges: 5 easy, 2 medium, 2 hard)

| Model | Easy | Medium | Hard | Expert | Total |
|---|---|---|---|---|---|
| Sonnet 4.5 | 2/2 | 0/2 | 0/3 | — | 2/7 |
| Opus 4.5 | 2/2 | 1/3 | 0/1 | — | 3/7 |
| Opus 4.6 | 2/2 | 2/3 | 1/1 | 0/1 | 5/7 |
| Sonnet 4.6 | 2/2 | 2/3 | 1/1 | 0/1 | 5/7 |

### Rev (8 challenges: 5 easy, 2 medium, 1 hard)

| Model | Easy | Medium | Hard | Total |
|---|---|---|---|---|
| Sonnet 4.5 | 3/3 | 2/2 | 0/1 | 5/6 |
| Opus 4.5 | 3/3 | 1/1 | 2/2 | 6/6 |
| Opus 4.6 | 3/3 | 1/1 | 2/2 | 6/6 |
| Sonnet 4.6 | 3/3 | 1/1 | 2/2 | 6/6 |

### Network (4 challenges: 1 easy, 3 medium)

| Model | Easy | Medium | Hard | Total |
|---|---|---|---|---|
| Sonnet 4.5 | 1/1 | 2/3 | 0/1 | 3/5 |
| Opus 4.5 | 1/1 | 3/3 | 0/1 | 4/5 |
| Opus 4.6 | 1/1 | 3/3 | 1/1 | 5/5 |
| Sonnet 4.6 | 1/1 | 3/3 | 1/1 | 5/5 |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) Figures 8.4.2-8.4.6; [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Figures 6.4.2-6.4.6. Difficulty breakdown from stacked bar charts. Note: "Total" column counts unique challenges solved at pass@30 (best-of-30 trials). Network shows 5 total despite only 4 described challenges, suggesting an additional challenge or sub-task.

---

## Aggregate Cyber Challenge Success Rates by Category (pass@30)

| Category | Sonnet 4.5 | Opus 4.5 | Opus 4.6 | Sonnet 4.6 |
|---|---|---|---|---|
| PWN | ~29% | ~43% | ~71% | ~71% |
| WEB | ~85% | ~92% | 100% | ~95% |
| CRYPTO | ~78% | ~83% | ~94% | ~96% |
| REV | ~83% | ~97% | 100% | 100% |
| NETWORK | ~60% | ~80% | 100% | 100% |
| MISC | ~67% | 100% | 100% | 100% |
| FORENSICS | 100% | 100% | 100% | 100% |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) Figure 8.4.6.B (p201); [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Figure 6.4.6.B (p124). Values approximated from bar charts. Cumulative scores across all CTF challenges including Cybench subset. Sonnet 4.6 performs comparably to Opus 4.6 across all categories.

---

## Key Milestones

- **First ASL-3 model**: Claude Opus 4 (2025-05) -- exceeded ASL-3 thresholds in cyber and CBRN
- **First real CTF competition entries**: PicoCTF 2025, HackTheBox AI vs Human (2025)
- **First autonomous Equifax breach reproduction**: Claude Sonnet 4.5 (2025-09) -- 2/5 trials
- **First successful network challenge without human assistance**: Claude Opus 4.5 (2025-11)
- **First real-world adversary use documented**: 2025-08 -- Chinese state-sponsored GTG-1002
- **First 500+ zero-day discovery**: Claude Opus 4.6 (2026-02)
- **First CAISI external cyber assessment**: Claude Opus 4.6 (2026-02) -- US Center for AI Standards and Innovation + US Government partners, novel vulnerabilities discovered
- **Highest Cybench score**: Claude Opus 4.6 at 93% pass@1, ~100% pass@30 (2026-02) -- benchmark saturated
- **Highest CyberGym score**: Claude Opus 4.6 at 66.6% pass@1 (2026-02)
- **Best prompt injection resistance (coding)**: Claude Opus 4.6 at 0.0% ASR in coding (all configurations); Claude Sonnet 4.6 matches Opus-level PI resistance in extended thinking (2026-02)
- **Best prompt injection resistance (computer use)**: Claude Sonnet 4.6 at 12.0%/42.9% ASR (ext thinking, no safeguards) -- outperforms Opus 4.6 (17.8%/78.6%) (2026-02)
- **Best ART benchmark robustness**: Claude Opus 4.6 at k=1: 0.2% (lowest single-attempt attack success among all models tested) (2026-02)
- **First Sonnet-class model with Opus-level PI defense**: Claude Sonnet 4.6 (2026-02)
- **Highest malicious computer use refusal rate**: Claude Sonnet 4.6 at 99.38% (2026-02) -- surpasses all previous models including Opus 4.6 (88.34%)
- **First Sonnet-class ASL-3 model**: Claude Sonnet 4.6 (2026-02) -- deployed under ASL-3 Standard
