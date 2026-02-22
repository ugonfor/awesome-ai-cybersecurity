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
  | Cybench | AI4Security > Offensive Capability | 76.5% | pass@10, 40 professional CTF tasks | System Card |
  | CyberGym ($2 cost limit) | AI4Security > Offensive Capability | 28.9% SOTA | Real-world CVE detection, $2 cost cap | System Card |
  | CyberGym (30 trials) | AI4Security > Offensive Capability | 66.7% vuln reproduction | 30 trial attempts, no cost limit | System Card |
  | CyberGym (30 trials, new vulns) | AI4Security > Offensive Capability | 33%+ new vuln discovery | 30 trial attempts | System Card |
  | CMU Cyber Ranges | AI4Security > Offensive Capability | Evaluated | ~50-host network simulations | System Card |
  | Equifax Simulation | AI4Security > Offensive Capability | 2/5 autonomous | 5 independent trial runs | System Card |

- **Agent Setup**: Agentic setup with standard Kali Linux tools; operates on ~50-host network simulations; Equifax simulation used only publicly disclosed CVE exploitation
- **Key Findings**: Cybench score doubled from 3.7 Sonnet's 35.9% to 76.5%; SOTA on CyberGym; first to demonstrate autonomous Equifax breach reproduction (2/5 trials); single-attempt success rate higher than Opus 4.1 with ten attempts
- **Notes**: CyberGym created by UC Berkeley RDI (1,507 known CVEs). CMU Cyber Ranges developed collaboratively with Carnegie Mellon University's CyLab and Incalmo.

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

- **Agent Setup**: Standard prompting
- **Key Findings**: Remains ASL-2; 87.7% appropriate assistance rate on legitimate security research queries

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
  | CyberGym | AI4Security > Offensive Capability | 50.63% pass@1 | pass@1, real-world CVE detection | System Card |
  | Network challenges | AI4Security > Offensive Capability | First unassisted solve | Multi-host network infiltration | System Card |
  | Cyber-harness network challenges | AI4Security > Offensive Capability | Evaluated | Network scenarios | System Card |

- **Agent Setup**: Agentic setup with network tools and cyber harness
- **Key Findings**: First successful network challenge solve without human assistance; 82% Cybench pass@1; 50.63% CyberGym pass@1

### 13. Claude Opus 4.6 System Card

- **Date**: 2026-02
- **URL**: [Web](https://anthropic.com/claude-opus-4-6-system-card) | [PDF](https://www-cdn.anthropic.com/0dd865075ad3132672ee0ab40b05a53f14cf5288.pdf)
- **Models**: Claude Opus 4.6
- **Type**: System Card
- **Cyber Risk Level**: ASL-3
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Cybench | AI4Security > Offensive Capability | 93% pass@1 (37 tasks) | pass@1, 37 professional CTF tasks | System Card |
  | CyberGym | AI4Security > Offensive Capability | Evaluated (1,507 CVEs) | Real-world CVE detection | System Card |
  | 40 Cybersecurity Investigations | AI4Security > Defensive Capability | 38/40 blind-ranked best | Blind-ranked comparisons | System Card |
  | Zero-day Discovery | Security4AI > Misuse Risk | 500+ zero-days | Pre-release testing | System Card |
  | 6 new cybersecurity probes | AI4Security > Offensive Capability | Evaluated | New probe evaluations | System Card |

- **Agent Setup**: Full agentic setup with network tools, vulnerability scanning, and investigation capabilities
- **Key Findings**: Cybench 93% pass@1 (highest reported for any model); best in 38/40 blind-ranked cybersecurity investigations; 500+ zero-day vulnerabilities discovered in pre-release testing; 213-page system card

### 14. Claude Sonnet 4.6 System Card

- **Date**: 2026-02-17
- **URL**: [Web](https://anthropic.com/claude-sonnet-4-6-system-card) | [PDF](https://www-cdn.anthropic.com/78073f739564e986ff3e28522761a7a0b4484f84.pdf)
- **Models**: Claude Sonnet 4.6
- **Type**: System Card
- **Cyber Risk Level**: ASL-2
- **Benchmarks Reported**:

  | Benchmark | Category | Score | Methodology | Source Page/Section |
  |---|---|---|---|---|
  | Prompt injection (coding + extended thinking) | Security4AI > Model Robustness | 0% attack success | Coding environment with extended thinking | System Card |
  | Prompt injection (browser) | Security4AI > Model Robustness | <0.3% attack success | Browser-based evaluation | System Card |

- **Agent Setup**: Evaluated in coding and browser environments with extended thinking
- **Key Findings**: Near-perfect prompt injection resistance: 0% in coding with extended thinking, <0.3% in browser environments

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
  | CyberGym (Sonnet 4) | AI4Security > Offensive Capability | Strongest on public leaderboard | Public leaderboard ranking | AI for Cyber Defenders |
  | CyberGym ($2 cost, Sonnet 4.5) | AI4Security > Offensive Capability | 28.9% SOTA | $2 cost limit per challenge | AI for Cyber Defenders |
  | CyberGym (30 trials, Sonnet 4.5) | AI4Security > Offensive Capability | 66.7% vuln reproduction | 30 trial attempts | AI for Cyber Defenders |
  | CyberGym (30 trials, new vulns, Sonnet 4.5) | AI4Security > Offensive Capability | 33%+ new vuln discovery | 30 trial attempts | AI for Cyber Defenders |

- **Agent Setup**: Automated vulnerability detection agent against real open-source codebases
- **Key Findings**: Claude Sonnet 4 strongest on CyberGym public leaderboard; Sonnet 4.5 achieved SOTA 28.9% at $2 cost; 66.7% vulnerability reproduction rate; 33%+ previously unknown vulnerability discovery
- **Notes**: CyberGym created by UC Berkeley RDI, NOT Anthropic. Contains 1,507 known CVEs.

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
| Claude Sonnet 4.5 | 2025-09 | 76.5% | pass@10, 40 tasks | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.5 | 2025-11 | 82% | pass@1, tasks | [System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Opus 4.6 | 2026-02 | 93% | pass@1, 37 tasks | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

---

## Key Milestones

- **First ASL-3 model**: Claude Opus 4 (2025-05) -- exceeded ASL-3 thresholds in cyber and CBRN
- **First real CTF competition entries**: PicoCTF 2025, HackTheBox AI vs Human (2025)
- **First autonomous Equifax breach reproduction**: Claude Sonnet 4.5 (2025-09) -- 2/5 trials
- **First successful network challenge without human assistance**: Claude Opus 4.5 (2025-11)
- **First real-world adversary use documented**: 2025-08 -- Chinese state-sponsored GTG-1002
- **First 500+ zero-day discovery**: Claude Opus 4.6 (2026-02)
- **Highest Cybench score**: Claude Opus 4.6 at 93% pass@1 (2026-02)
- **Best prompt injection resistance**: Claude Sonnet 4.6 at 0% attack success in coding with extended thinking (2026-02)
