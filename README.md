# Awesome AI Cybersecurity [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated AI cybersecurity benchmarks, agents & tools — organized by Security OF / BY / FROM AI

The AI cybersecurity space is fragmented: OpenAI, Anthropic, Google, and xAI each use different benchmarks, and terms like "red team," "blue team," "safety," and "security" are used inconsistently. This repo cuts through the confusion with a clear taxonomy and comprehensive cross-comparison.

---

## Contents

- [Taxonomy](#taxonomy)
- [Cross-Comparison](#cross-comparison)
  - [Model Cyber Capability Leaderboard](#model-cyber-capability-leaderboard)
  - [Risk Frameworks](#risk-frameworks)
  - [Benchmark Mapping](#benchmark-mapping) (collapsible)
  - [Timeline](#timeline) (collapsible)
- [Benchmarks](#benchmarks)
  - [Security OF AI](#security-of-ai)
  - [Security BY AI](#security-by-ai)
  - [Security FROM AI](#security-from-ai)
- [Agents — Security BY AI](#agents--security-by-ai)
- [Tools](#tools)
- [Vendor Documentation](#vendor-documentation)

---

## Taxonomy

The core differentiator of this repo. We classify everything along two axes:

### Axis 1: Whose security?

| Category | Meaning | Example |
|----------|---------|---------|
| **Security OF AI** | Protecting the AI model itself | Jailbreak defense, prompt injection robustness |
| **Security BY AI** | AI performing cybersecurity tasks | CTF solving, vulnerability analysis, SOC automation |
| **Security FROM AI** | Assessing risks posed by AI | Malware generation capability, exploit writing risk |

### Axis 2: Offensive vs Defensive

| Category | Meaning |
|----------|---------|
| **Offensive (Red Team)** | Attack simulation, vulnerability discovery |
| **Defensive (Blue Team)** | Detection, analysis, incident response |
| **Evaluation** | Pure capability measurement |

---

## Cross-Comparison

### Model Cyber Capability Leaderboard

> Side-by-side comparison of frontier models. Every score links to its source. "Agent" = the evaluation setup (base model, agentic scaffold, or specialized variant).

| | Model | Agent | Date | CTF (Pro) | [Cybench](https://cybench.github.io/) | [CVE-Bench](benchmarks/security-by-ai/offensive/) | Cyber Range | [HTB](https://www.hackthebox.com/) | Vuln Discovery | [WMDP-Cyber](https://www.wmdp.ai/) |
|---|---|---|---|---|---|---|---|---|---|---|
| **OpenAI** | GPT-5.3-Codex | Codex | 2026.02 | [All passed](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) | — | — | [All except 3](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) | — | — | — |
| | GPT-5.2-Codex | Codex | 2025.12 | — | — | [87%](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) | — | — | — | — |
| | GPT-5.1-Codex-Max | Codex | 2025.11 | [~76%](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) | — | — | [37%](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) | — | — | — |
| | GPT-5-Codex | Codex | 2025.09 | ["sharp jump"](https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf) | — | — | — | — | — | — |
| | GPT-5 | Base | 2025.08 | [~27%](https://cdn.openai.com/gpt-5-system-card.pdf) | — | — | — | — | — | — |
| | o3 | Base | 2025.04 | [~58%](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) | — | — | — | — | — | — |
| | Deep Research | o3 + browse | 2025.02 | [70%](https://cdn.openai.com/deep-research-system-card.pdf) | — | — | — | — | — | — |
| **Anthropic** | Claude Opus 4.6 | Base | 2026.02 | — | — | — | — | — | [500+ zero-days](https://anthropic.com/claude-opus-4-6-system-card) | — |
| | Claude Sonnet 4.6 | Base | 2026.02 | — | — | — | — | — | [0% prompt inj.](https://anthropic.com/claude-sonnet-4-6-system-card) | — |
| | Claude Opus 4.5 | Base | 2025.11 | — | — | — | [1st auto solve](https://www.anthropic.com/claude-opus-4-5-system-card) | — | — | — |
| | Claude Sonnet 4.5 | Base | 2025.09 | — | [76.5%](https://www.anthropic.com/claude-sonnet-4-5-system-card) | — | [2/5 Equifax](https://www.anthropic.com/claude-sonnet-4-5-system-card) | — | [28.9% CyberGym](https://red.anthropic.com/2025/ai-for-cyber-defenders/) | — |
| | Claude Opus 4.1 | Base | 2025.08 | — | [ASL-3](https://www.anthropic.com/claude-opus-4-1-system-card) | — | — | — | — | — |
| | Claude Opus 4 | Base | 2025.05 | [11/11,1/2,0/2](https://www.anthropic.com/claude-4-system-card) | — | — | — | — | — | — |
| | Claude Sonnet 4 | Base | 2025.05 | [10/11,1/2,0/2](https://www.anthropic.com/claude-4-system-card) | — | — | — | — | — | — |
| | Claude 3.7 Sonnet | Base | 2025.02 | — | [35.9%](https://anthropic.com/claude-3-7-sonnet-system-card) | — | — | — | — | — |
| **Google** | Gemini 3.1 Pro | Base | 2026.02 | — | — | — | — | [> 3 Pro](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf) | — | — |
| | Gemini 3 Pro | Base | 2025.11 | — | — | — | — | [11/12](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) | — | — |
| | Gemini 2.5 DT | Deep Think | 2025.08 | [13/13 GDM](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) | — | — | — | [3/13](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) | — | — |
| | Gemini 2.5 Pro | Base | 2025.06 | [76/76 ICF](https://modelcards.withgoogle.com/assets/documents/gemini-2.5-pro.pdf) | — | — | — | [6/12](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) | — | — |
| | Gemini 2.0 Flash | Base | 2025.04 | — | — | — | — | — | [11/50 PatternLabs](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf) | — |
| **xAI** | Grok 4.1 | UK AISI Inspect | 2025.11 | — | [< experts](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) | — | — | — | — | [87% (Bio)](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| | Grok 4 Fast | UK AISI Inspect | 2025.09 | — | — | — | — | — | — | [81.4%](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| | Grok 4 | UK AISI Inspect | 2025.08 | — | [< human](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) | — | — | — | — | [79%](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |

---

### Risk Frameworks

Each company has its own framework for evaluating cybersecurity risk:

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **Framework** | [Preparedness Framework v2](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf) | [RSP v2.2](https://www.anthropic.com/responsible-scaling-policy) | [FSF v3.0](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf) | [Risk Management Framework](https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf) |
| **Risk Levels** | Low → Medium → High → Critical | ASL-1 → ASL-2 → ASL-3 → ASL-4 | CCL alert → CCL reached | Abuse / Propensities / Dual-use |
| **Cyber Threshold** | High: automate end-to-end ops against hardened targets OR zero-day discovery | ASL-3: ≥1/5 success in ≥2/6 expert exploit dev classes | Cyber Uplift L1: ≥10x cost reduction for high-impact attacks | Not explicitly defined |
| **First Crossed** | GPT-5.3-Codex (Feb 2026) — **HIGH** | Claude Opus 4 (May 2025) — **ASL-3** | None (alert only) | None |
| **Third-party** | US/UK AISI | US/UK AISI, METR | — | UK AISI |

### Benchmark Mapping

> **Key Insight: There is virtually no overlap in quantitative benchmarks across companies.**

<details>
<summary>Which company uses which benchmark? (click to expand)</summary>

#### Security BY AI — Offensive (Cyber Capability)

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **CTF (internal/custom)** | ✅ | ✅ | ✅ | — | Each company's proprietary CTF challenge sets |
| **[Cybench](https://cybench.github.io/)** | — | ✅ | — | ✅ | 40 professional CTF tasks from 4 competitions (xAI spells it "CyBench") |
| **[CyberGym](https://red.anthropic.com/2025/ai-for-cyber-defenders/)** | — | ✅ | — | — | Real-world vuln detection in open-source software |
| **CVE-Bench** | ✅ | — | — | — | Exploit real-world web app CVEs (pass@1) |
| **Cyber Range** | ✅ | ✅ | — | — | Multi-machine network attack scenarios |
| **[InterCode-CTF](https://arxiv.org/abs/2306.14898)** | — | — | ✅ | — | 76 easy CTF challenges (largely saturated) |
| **[In-house CTF (GDM)](https://github.com/google-deepmind/dangerous-capability-evaluations)** | — | — | ✅ | — | 13 medium challenges (open-sourced via UK AISI Inspect) |
| **Hack the Box** | — | ✅ | ✅ | — | Professional-level CTF challenges |
| **Key Skills Benchmark** | — | — | ✅ | — | Recon, tool dev, OPSEC (MITRE ATT&CK aligned) |
| **Pattern Labs External CTFs** | — | — | ✅ | — | 50 non-public challenges (anti-contamination) |
| **PicoCTF / HTB / WRCCDC** | — | ✅ | — | — | Real competitive CTF events |
| **Equifax Simulation** | — | ✅ | — | — | High-fidelity breach simulation |
| **CMU Cyber Ranges** | — | ✅ | — | — | ~50-host network simulations |

#### Security BY AI — Knowledge

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **[WMDP-Cyber](https://www.wmdp.ai/)** | — | — | — | ✅ | Cyber killchain MC questions |
| **MC Cybersecurity Knowledge** | ✅ | — | — | — | OpenAI internal MC eval |
| **CTI-MCQ** | — | — | ✅ | — | Threat intelligence knowledge (Sec-Gemini) |
| **CTI-RCM** | — | — | ✅ | — | Root cause → CWE mapping (Sec-Gemini) |

#### Security OF AI — Jailbreak / Prompt Injection / Robustness

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **Prompt Injection Eval** | ✅ | ✅ | ✅ | — | Robustness to prompt injection attacks |
| **[TAP](https://arxiv.org/abs/2312.02119) Attack Success Rate** | — | — | ✅ | — | Tree of Attacks with Pruning |
| **[AgentDojo](https://arxiv.org/abs/2406.13352)** | — | — | — | ✅ | Prompt injection in agentic settings |
| **Jailbreak Robustness** | ✅ | ✅ | — | — | Universal jailbreak resistance testing |
| **Automated Red Teaming (ART)** | — | — | ✅ | — | Continuous adversarial evaluation framework |
| **Expert Red Teaming** | ✅ | ✅ | ✅ | — | External experts adversarially testing models |

#### Security FROM AI — Misuse Risk / Dual-use

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **[AgentHarm](https://arxiv.org/abs/2410.09024)** | — | — | — | ✅ | Malicious agentic task completion |
| **Malware Benchmark** | ✅ | — | — | — | Synthetic malware-related task eval (Codex) |
| **Harmful Request Refusal** | ✅ | ✅ | ✅ | ✅ | Refusal rate on violative/harmful prompts |
| **Zero-day Discovery Eval** | — | ✅ | — | — | Model auditing OSS for novel vulns |

#### Security FROM AI — Behavioral / Alignment

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **[MASK](https://arxiv.org/abs/2503.03750)** | — | — | — | ✅ | Deception measurement under pressure |
| **MakeMeSay** | — | — | — | ✅ | Persuasion / manipulation eval |
| **Sycophancy Eval** | — | — | — | ✅ | Ignoring own judgment for user agreement |
| **Stealth Eval** | — | — | ✅ | — | Ability to circumvent oversight |
| **Situational Awareness** | — | — | ✅ | — | Self/environment reasoning |
| **Sabotage Risk** | — | ✅ | — | — | 9 sabotage pathways (METR-reviewed) |

#### Benchmark Overlap Summary

| Overlap | Benchmarks |
|---|---|
| **4 companies** | Harmful Request Refusal (each with internal version) |
| **3 companies** | Expert Red Teaming, Prompt Injection Eval |
| **2 companies** | Cybench (Anthropic + xAI), Cyber Range, Jailbreak Robustness |
| **1 company only** | CVE-Bench, CyberGym, InterCode-CTF, WMDP-Cyber, AgentHarm, CTI-MCQ/RCM |

</details>

### Reported Performance Numbers

<details>
<summary>Detailed benchmark-by-benchmark results with sources</summary>

#### CTF Performance

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-4o | OpenAI | Custom CTF (HS/Coll/Pro) | 19% / 0% / 1% | 2024.08 | [System Card](https://cdn.openai.com/gpt-4o-system-card.pdf) |
| o1-preview | OpenAI | Custom CTF (HS/Coll/Pro) | 26.7% / 0% / 2.5% | 2024.09 | [System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1-mini | OpenAI | Custom CTF (HS/Coll/Pro) | 28.7% / 0% / 3.9% | 2024.09 | [System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1 | OpenAI | Custom CTF (HS/Coll/Pro) | 46% / 13% / 13% | 2024.12 | [System Card](https://cdn.openai.com/o1-system-card-20241205.pdf) |
| o3-mini | OpenAI | Custom CTF (HS/Coll) | 61% / 21% | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Deep Research (no browse) | OpenAI | Custom CTF (HS/Coll/Pro) | 82% / 55% / 47% | 2025.02 | [System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| Deep Research (w/ browse) | OpenAI | Custom CTF (HS/Coll/Pro) | 92% / 91% / 70% | 2025.02 | [System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| o3 | OpenAI | Custom CTF (Professional) | ~58% | 2025.04 | [System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| GPT-5 | OpenAI | Custom CTF (Professional, pass@12) | ~27% | 2025.08 | [System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5-Codex | OpenAI | Custom CTF + CVE-Bench + Cyber Range | "Sharp jump" | 2025.09 | [Addendum](https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Custom CTF (Professional) | ~76% (17/18 easy, 9/17 med, 0/6 hard) | 2025.11 | [System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Custom CTF (Professional) | All passed | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude 3.7 Sonnet | Anthropic | Cybench (40 tasks) | 35.9% | 2025.02 | [System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
| Claude Opus 4 | Anthropic | Custom CTF | 11/11 easy, 1/2 med, 0/2 hard | 2025.05 | [System Card](https://www.anthropic.com/claude-4-system-card) |
| Claude Sonnet 4 | Anthropic | Custom CTF | 10/11 easy, 1/2 med, 0/2 hard | 2025.05 | [System Card](https://www.anthropic.com/claude-4-system-card) |
| Claude Sonnet 4.5 | Anthropic | Cybench (40 tasks) | 76.5% | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Gemini 2.0 Flash | Google | Pattern Labs External CTFs | 11/50 | 2025.04 | [Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf) |
| Gemini 2.5 Pro | Google | InterCode-CTF | 76/76 (saturated) | 2025.06 | [Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2.5-pro.pdf) |
| Gemini 2.5 Pro | Google | Hack the Box (Hard) | 6/12 | 2025.06 | [FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
| Gemini 2.5 Deep Think | Google | InterCode-CTF | 73/76 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | In-house CTF (Medium, 13) | 13/13 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | Hack the Box (Hard) | 3/13 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 3 Pro | Google | Hack the Box (Hard) | 11/12 | 2025.11 | [FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |

#### CVE / Vulnerability Benchmarks

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.2-Codex | OpenAI | CVE-Bench (pass@1) | 87% | 2025.12 | [Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| Claude Sonnet 4.5 | Anthropic | CyberGym ($2 cost) | 28.9% | 2025.09 | [Frontier Red Team](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials) | 66.7% vuln reproduction, 33%+ new vuln discovery | 2025.09 | [Frontier Red Team](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Opus 4.6 | Anthropic | Zero-day discovery | 500+ novel vulns | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

#### Cyber Range / End-to-End Attack

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.1-Codex-Max | OpenAI | Cyber Range (Network/Vuln/Evasion) | 37% / 41% / 43% | 2025.11 | [System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Cyber Range | All except 3 (EDR, CA/DNS, Leaked Token) | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | Equifax Simulation | 2/5 autonomous | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |

#### Real-World Competitions / Investigations

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Claude | Anthropic | PicoCTF 2025 | Top 3% (297th/10,460), 32/41 challenges | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | HackTheBox AI vs Human | 30th/161, 4th/8 AI teams, 19/20 solved | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | WRCCDC | 6th/9 teams | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude Opus 4.6 | Anthropic | 40 cyber investigations | 38/40 best (blind-ranked) | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

#### Cybersecurity Knowledge

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o3-mini | OpenAI | MC Cybersecurity Knowledge | 53% | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| o1 | OpenAI | MC Cybersecurity Knowledge | 59% | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Grok 4 | xAI | WMDP-Cyber | 79% | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | WMDP-Cyber | 81.4% | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Sec-Gemini v1 | Google | CTI-MCQ | +11% over competitors | 2025.04 | [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |
| Sec-Gemini v1 | Google | CTI-RCM | +10.5% over competitors | 2025.04 | [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

#### Prompt Injection / Robustness

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Operator (GPT-4o) | OpenAI | Prompt Injection | 99% recall | 2025.01 | [System Card](https://cdn.openai.com/operator_system_card.pdf) |
| Gemini 2.0 → 2.5 | Google | TAP Attack Success | 99.8% → 53.6% | 2025.05 | [Paper](https://arxiv.org/abs/2505.14534) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (coding) | 0% attack success | 2026.02 | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (browser) | <0.3% attack success | 2026.02 | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Grok 4 Fast | xAI | AgentDojo | 0–3% attack success | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |

#### Misuse / Behavioral

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Grok 4 Fast | xAI | AgentHarm | 8–10% completion | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4 | xAI | MASK (deception) | 0.43 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 | xAI | Sycophancy | 0.07 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4.1 | xAI | AgentHarm | <14% | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 | xAI | MASK (deception) | 0.49 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 | xAI | MakeMeSay | 0% (as attacker) | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 | xAI | Sycophancy | 0.19 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

</details>

<details>
<summary>Documentation Maturity & Timeline</summary>

### Documentation Maturity

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **First cyber benchmark** | GPT-4o (Aug 2024) | Claude 3 (Mar 2024) | Phuong et al. (Mar 2024) | Grok 4 (Aug 2025) |
| **Documents w/ cyber evals** | 19 | 24 | 25+ | 9 |
| **Open-sources evals?** | No | No | Yes (In-house CTF via Inspect) | No |
| **Real-world threat intel?** | No | Yes (GTG-1002) | Yes (12,000+ incidents) | No |
| **Specialized cyber model?** | Aardvark (private beta) | — | Sec-Gemini v1 | — |

### Timeline

| Date | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| 2023.03 | GPT-4: Low | — | — | — |
| 2023.07 | — | Claude 2: qualitative | — | — |
| 2023.12 | — | — | Gemini 1.0: rudimentary | Grok-1: no eval |
| 2024.03 | — | Claude 3: ASL-2 | Gemini 1.0: early warning | — |
| 2024.08 | GPT-4o: Low | — | — | — |
| 2024.09 | o1: Low | — | — | — |
| 2025.01 | o3-mini: Low | — | — | — |
| 2025.02 | Deep Research: **Medium** | Claude 3.7: ASL-2 | — | — |
| 2025.04 | o3: Below High | — | Gemini 2.5 Pro: CCL alert | — |
| 2025.05 | — | Opus 4: **ASL-3** | — | — |
| 2025.08 | GPT-5: Below High | — | Gemini 2.5 DT: CCL alert | Grok 4: below human pro |
| 2025.11 | GPT-5.1: Below High | Opus 4.5: ASL-3 | Gemini 3 Pro: CCL alert | Grok 4.1: below human pro |
| 2026.02 | GPT-5.3: **HIGH** | Opus 4.6: ASL-3 | Gemini 3.1 Pro: CCL alert | — |

</details>

---

## Benchmarks

> 70+ benchmarks across three categories. Vendor-specific benchmarks are mapped in [Cross-Comparison](#benchmark-mapping) above.

| Category | Scope | Vendor | Academic | Full List |
|---|---|:---:|:---:|---|
| **Security OF AI** | Jailbreak, prompt injection, adversarial robustness | 6 | 14 | [`benchmarks/security-of-ai/`](benchmarks/security-of-ai/) |
| **Security BY AI** | CTF, pentest, vuln detection, threat intel knowledge | 19 | 18 | [`benchmarks/security-by-ai/`](benchmarks/security-by-ai/) |
| **Security FROM AI** | Misuse risk, dual-use, deception, alignment | 10 | 3 | [`benchmarks/security-from-ai/`](benchmarks/security-from-ai/) |

**Notable academic benchmarks** (not used by the 4 major vendors):

| Benchmark | Category | Scale | Venue |
|---|---|---|---|
| [HarmBench](https://github.com/centerforaisafety/HarmBench) | OF AI — Jailbreak | 510 behaviors, 18 attacks, 33 LLMs | ICML 2024 |
| [CyberSecEval v1-v4](https://github.com/meta-llama/PurpleLlama) | OF AI — Secure Code | ~1,000+ test cases | Meta |
| [NYU CTF Bench](https://github.com/NYU-LLM-CTF/NYU_CTF_Bench) | BY AI — CTF | 200 challenges, 6 categories | NeurIPS 2024 |
| [SecBench](https://github.com/secbench-git/SecBench) | BY AI — Knowledge | 47,910 questions, 9 domains | — |
| [PrimeVul](https://github.com/DLVulDet/PrimeVul) | BY AI — Vuln Detection | 7K vuln + 229K benign functions | ICSE 2025 |
| [DecodingTrust](https://github.com/AI-secure/DecodingTrust) | OF AI — Trust | 8 dimensions | NeurIPS 2023 Outstanding (D&B Track) |

---

## Agents — Security BY AI

> AI performing cybersecurity tasks (Axis 1: BY AI). Classified by Axis 2: Offensive / Defensive. 39 agents total — full details in [`agents/`](agents/).

### Agent Performance Leaderboard

| Agent | Benchmark | Score | vs Human | Source |
|---|---|---|---|---|
| **[XBOW](https://xbow.com/)** | [HackerOne](https://www.hackerone.com/) bug bounty | #1 leaderboard (1,060 reports) | Outperformed all humans | [Blog](https://xbow.com/blog/top-1-how-xbow-did-it) |
| **[ARTEMIS](https://github.com/Stanford-Trinity/ARTEMIS)** | Enterprise pentest (8K hosts) | 2nd/11, 9 vulns found | Beat 9/10 humans, 1/3 cost | [Paper](https://arxiv.org/abs/2512.09882) |
| **[D-CIPHER](https://github.com/NYU-LLM-CTF/nyuctf_agents)** | [NYU CTF](https://github.com/NYU-LLM-CTF/NYU_CTF_Bench) / [Cybench](https://cybench.github.io/) / [HTB](https://www.hackthebox.com/) | 22% / 22.5% / 44% | — | [Paper](https://arxiv.org/abs/2502.10931) |
| **[Big Sleep](https://projectzero.google/2024/10/from-naptime-to-big-sleep.html)** | Real-world vuln discovery | First AI zero-day (SQLite) | Novel capability | [Blog](https://projectzero.google/2024/10/from-naptime-to-big-sleep.html) |
| **[Project Ire](https://www.microsoft.com/en-us/research/blog/project-ire-autonomously-identifies-malware-at-scale/)** | Malware RE | Precision 0.98, recall 0.83 | First AI malware conviction | [Blog](https://www.microsoft.com/en-us/research/blog/project-ire-autonomously-identifies-malware-at-scale/) |
| **[Security Copilot](https://www.microsoft.com/en-us/security/business/ai-machine-learning/microsoft-copilot-security)** | Phishing triage | 77% accuracy improvement | 40+ hrs/week saved | [Microsoft](https://www.microsoft.com/en-us/security/business/ai-machine-learning/microsoft-copilot-security) |
| **[CAI](https://github.com/aliasrobotics/cai)** | CTF benchmarks | 3,600x human speed | — | [Paper](https://arxiv.org/abs/2504.06017) |

### Offensive — Top Picks

| Agent | Why it matters |
|---|---|
| **[XBOW](https://xbow.com/)** | #1 on HackerOne leaderboard 2025 — found vulns in Amazon, Disney, PayPal |
| **[ARTEMIS](https://github.com/Stanford-Trinity/ARTEMIS)** | Beat 9/10 human pentesters in live enterprise test at 1/3 the cost |
| **[D-CIPHER](https://github.com/NYU-LLM-CTF/nyuctf_agents)** | SOTA on NYU CTF (22%), Cybench (22.5%), HackTheBox (44%) |
| **[PentestGPT](https://github.com/GreyDGL/PentestGPT)** | First LLM pentest agent — USENIX Security 2024 |
| **[CAI](https://github.com/aliasrobotics/cai)** | Open-source, 300+ models, 3,600x over human pentesters |

<details>
<summary>16 more offensive agents</summary>

| Agent | Created by | Open Source |
|---|---|:---:|
| [AutoPentester](https://github.com/YasodGinige/AutoPentester) | Univ. Sydney | Yes |
| [SWE-agent / EnIGMA](https://github.com/SWE-agent/SWE-agent) | Princeton/NYU/TAU | Yes |
| [PentAGI](https://github.com/vxcontrol/pentagi) | VXControl | Yes |
| [CRAKEN](https://github.com/NYU-LLM-CTF/nyuctf_agents_craken) | NYU | Yes |
| [Reaper](https://github.com/ghostsecurity/reaper) | Ghost Security | Yes |
| [Strix](https://github.com/usestrix/strix) | usestrix | Yes |
| [hackingBuddyGPT](https://github.com/ipa-lab/hackingBuddyGPT) | TU Wien | Yes |
| [PentestAgent](https://github.com/GH05TCREW/pentestagent) | GH05TCREW | Yes |
| [HackerGPT](https://github.com/Hacker-GPT/HackerGPT-2.0) | Community | Yes |
| [ReaperAI](https://github.com/tac01337/ReaperAI) | tac01337 | Yes |
| [AutoAttacker](https://arxiv.org/abs/2403.01038) | UC researchers | No |
| [KryptoPilot](https://arxiv.org/abs/2601.09129) | Academic | — |
| [Penligent](https://penligent.ai/) | Penligent | No |
| [TARS](https://github.com/osgil-defense/TARS) | Osgil Defense | Yes |
| [Auto-Pentest-GPT](https://github.com/Armur-Ai/Auto-Pentest-GPT-AI) | Armur AI | Yes |
| [CIPHER](https://www.researchgate.net/publication/385337738) | Academic | — |

</details>

### Defensive — Top Picks

| Agent | Why it matters |
|---|---|
| **[Big Sleep](https://projectzero.google/2024/10/from-naptime-to-big-sleep.html)** | First AI-discovered real-world zero-day (SQLite) — Google P0 + DeepMind |
| **[Microsoft Security Copilot](https://www.microsoft.com/en-us/security/business/ai-machine-learning/microsoft-copilot-security)** | 37+ agents, Phishing Triage improves accuracy 77% |
| **[Project Ire](https://www.microsoft.com/en-us/research/blog/project-ire-autonomously-identifies-malware-at-scale/)** | Autonomous malware RE, precision 0.98 — Black Hat 2025 |
| **[Charlotte AI](https://www.crowdstrike.com/en-us/platform/charlotte-ai/)** | >98% triage accuracy, Agentic SOAR — CrowdStrike |
| **[Cortex XSIAM](https://www.paloaltonetworks.com/cortex/cortex-xsiam)** | Trained on 1.2B playbooks, 98% MTTR reduction — Palo Alto |

<details>
<summary>8 more defensive agents</summary>

| Agent | Created by |
|---|---|
| [Google TI Agentic](https://gtidocs.virustotal.com/docs/agentic-platform) | Google (Mandiant + VirusTotal) |
| [Sec-Gemini v1](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) | Google |
| [OpenAI Aardvark](https://openai.com/index/strengthening-cyber-resilience/) | OpenAI |
| [Dropzone AI](https://www.dropzone.ai) | Dropzone AI |
| [Exaforce](https://www.exaforce.com) | Exaforce |
| [Radiant Security](https://radiantsecurity.ai) | Radiant Security |
| [Simbian AI](https://simbian.ai) | Simbian |
| [Joe Reverser](https://www.joesecurity.org/joe-reverser) | Joe Security |

</details>

### Multi-Purpose

| Agent | Summary |
|---|---|
| **[Fabric](https://github.com/danielmiessler/fabric)** | 200+ prompt patterns for threat modeling, vuln analysis |
| **[Floki / Dapr Agents](https://github.com/Cyb3rWard0g/floki)** | Multi-agent framework, donated to CNCF |
| **[BurpGPT](https://github.com/aress31/burpgpt)** | Burp Suite + LLM passive scanning |
| **[Burp AI Agent](https://github.com/six2dez/burp-ai-agent)** | 53+ MCP tools, 62 vuln classes |

---

## Tools

> 20 tools and platforms. Full details in [`tools/`](tools/).

**Evaluation Frameworks** (cross-taxonomy):

| Tool | Created by | Summary |
|---|---|---|
| **[Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)** | UK AISI | Python framework for reproducible LLM evaluations with sandboxing |
| **[Inspect Cyber](https://inspect.cyber.aisi.org.uk/)** | UK AISI | Agentic cyber eval with CTF/cyber range YAML configs |
| **[Vivaria](https://github.com/METR/vivaria)** | METR | Agent evaluation platform (transitioning to Inspect) |
| **[lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness)** | EleutherAI | Unified LLM eval (includes WMDP-Cyber) |

**Security OF AI** — Testing model robustness:

| Tool | Created by | Summary |
|---|---|---|
| **[Garak](https://github.com/NVIDIA/garak)** | NVIDIA | LLM vulnerability scanner (prompt injection, jailbreak, data leakage) |
| **[Promptfoo](https://github.com/promptfoo/promptfoo)** | Open source | LLM red teaming CLI with OWASP Top 10 + CI/CD |
| **[HarmBench](https://github.com/centerforaisafety/HarmBench)** | CAIS | Standardized: 18 attacks vs 33 LLMs |
| **[JailbreakBench](https://github.com/JailbreakBench/jailbreakbench)** | Multi-institution | 100 behaviors + attack/defense leaderboard |
| **[StrongREJECT](https://github.com/dsbowen/strong_reject)** | UC Berkeley / GDM | Jailbreak eval with SOTA human agreement |

**Security BY AI** — Cybersecurity task platforms:

| Tool | Created by | Summary |
|---|---|---|
| **[PurpleLlama / CyberSecEval](https://github.com/meta-llama/PurpleLlama)** | Meta | Insecure code gen, SOC eval, auto-patching (v1-v4) |
| **[Hack The Box](https://www.hackthebox.com/)** | HTB | AI Range (Dec 2025) for autonomous agent benchmarking |
| **[picoCTF](https://picoctf.org/)** | CMU CyLab | 800,000+ users; Claude ranked top 3% in 2025 |
| **[CTFd](https://github.com/CTFd/CTFd)** | CTFd LLC | Most widely used CTF hosting framework |
| **[CyberBattleSim](https://github.com/microsoft/CyberBattleSim)** | Microsoft Research | OpenAI Gym for RL attack/defense simulation |
| **[ControlArena](https://control-arena.aisi.org.uk/)** | UK AISI + Redwood | AI control experiments for misalignment prevention |

<details>
<summary>More tools (benchmark suites, eval collections)</summary>

| Tool | Taxonomy | Created by |
|---|---|---|
| [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals) | Cross-taxonomy | UK AISI + community |
| [Dangerous Capability Evals](https://github.com/google-deepmind/dangerous-capability-evaluations) | FROM AI | Google DeepMind |
| [CAIBench](https://arxiv.org/abs/2510.24317) | BY AI | Alias Robotics |
| [ExCyTIn-Bench](https://github.com/microsoft/SecRL) | BY AI > Defensive | Microsoft |
| [eyeballvul](https://github.com/timothee-chauvin/eyeballvul) | BY AI > Offensive | METR-affiliated |

</details>

---

## Vendor Documentation

Detailed per-vendor documentation is available in [`raw-data/`](raw-data/):

- [`raw-data/openai.md`](raw-data/openai.md) — 19 documents, GPT-4 through GPT-5.3-Codex
- [`raw-data/anthropic.md`](raw-data/anthropic.md) — 24 documents, Claude 2 through Claude Opus 4.6
- [`raw-data/google.md`](raw-data/google.md) — 25+ documents, Gemini 1.0 through Gemini 3.1 Pro
- [`raw-data/xai.md`](raw-data/xai.md) — 9 documents, Grok-1 through Grok 4.1

---

## Contributing

Contributions welcome! Please follow the taxonomy (OF / BY / FROM) when adding new entries.

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
