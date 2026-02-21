# Awesome AI Cybersecurity [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated AI cybersecurity benchmarks, agents & tools — organized by Security OF / BY / FROM AI

The AI cybersecurity space is fragmented: OpenAI, Anthropic, Google, and xAI each use different benchmarks, and terms like "red team," "blue team," "safety," and "security" are used inconsistently. This repo cuts through the confusion with a clear taxonomy and comprehensive cross-comparison.

---

## Contents

- [Taxonomy](#taxonomy)
- [Cross-Comparison](#cross-comparison)
  - [Risk Frameworks](#risk-frameworks)
  - [Benchmark Mapping](#benchmark-mapping)
  - [Reported Performance Numbers](#reported-performance-numbers)
  - [Timeline](#timeline)
- [Benchmarks](#benchmarks)
  - [Security OF AI](#security-of-ai)
  - [Security BY AI](#security-by-ai)
  - [Security FROM AI](#security-from-ai)
- [Agents](#agents)
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

#### Security BY AI — Offensive (Cyber Capability)

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **CTF (internal/custom)** | ✅ | ✅ | ✅ | — | Each company's proprietary CTF challenge sets |
| **[Cybench](https://cybench.github.io/)** | — | ✅ | — | — | 40 professional CTF tasks from 4 competitions |
| **[CyBench](https://cybench.github.io/)** | — | — | — | ✅ | 40 CTF challenges (UK AISI Inspect). Note: different from Cybench |
| **[CyberGym](https://red.anthropic.com/2025/ai-for-cyber-defenders/)** | — | ✅ | — | — | Real-world vuln detection in open-source software |
| **CVE-Bench** | ✅ | — | — | — | Exploit real-world web app CVEs (pass@1) |
| **Cyber Range** | ✅ | ✅ | — | — | Multi-machine network attack scenarios |
| **[InterCode-CTF](https://arxiv.org/abs/2306.14898)** | — | — | ✅ | — | 76 easy CTF challenges (largely saturated) |
| **[In-house CTF (GDM)](https://github.com/google-deepmind/dangerous-capability-evaluations)** | — | — | ✅ | — | 13 medium challenges (open-sourced via UK AISI Inspect) |
| **Hack the Box** | — | — | ✅ | — | Professional-level CTF challenges |
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
| **[MASK](https://arxiv.org/abs/2406.11663)** | — | — | — | ✅ | Deception measurement under pressure |
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
| **2 companies** | Cyber Range, Jailbreak Robustness |
| **1 company only** | CVE-Bench, CyberGym, InterCode-CTF, WMDP-Cyber, AgentHarm, CTI-MCQ/RCM, Cybench, CyBench |

### Reported Performance Numbers

#### CTF Performance

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-4o | OpenAI | Custom CTF (Professional) | 1% | 2024.08 | [System Card](https://cdn.openai.com/gpt-4o-system-card.pdf) |
| o1-preview | OpenAI | Custom CTF (Professional) | 2.5% | 2024.09 | [System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1 | OpenAI | Custom CTF (Professional) | 13% | 2024.12 | [System Card](https://cdn.openai.com/o1-system-card-20241205.pdf) |
| Deep Research (no browse) | OpenAI | Custom CTF (Professional) | 47% | 2025.02 | [System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| Deep Research (w/ browse) | OpenAI | Custom CTF (Professional) | 70% | 2025.02 | [System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| o3 | OpenAI | Custom CTF (Professional) | ~58% | 2025.04 | [System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| GPT-5 | OpenAI | Custom CTF (Professional, pass@12) | ~27% | 2025.08 | [System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Custom CTF (Professional) | ~76% | 2025.11 | [System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Custom CTF (Professional) | All passed | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude 3.7 Sonnet | Anthropic | Cybench (40 tasks) | 35.9% | 2025.02 | [System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
| Claude Opus 4 | Anthropic | Custom CTF | 11/11 easy, 1/2 med, 0/2 hard | 2025.05 | [System Card](https://www.anthropic.com/claude-4-system-card) |
| Claude Sonnet 4.5 | Anthropic | Cybench (40 tasks) | 76.5% | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.6 | Anthropic | 40 cyber investigations | 38/40 best (blind-ranked) | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 2.5 Deep Think | Google | In-house CTF (Medium, 13) | 13/13 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | Hack the Box (Hard) | 3/13 | 2025.08 | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 3 Pro | Google | Hack the Box (Hard) | 11/12 | 2025.11 | [FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |

#### CVE / Vulnerability Benchmarks

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.2-Codex | OpenAI | CVE-Bench (pass@1) | 87% | 2025.12 | [Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| Claude Sonnet 4.5 | Anthropic | CyberGym ($2 cost) | 28.9% | 2025.09 | [Frontier Red Team](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials) | 66.7% vuln reproduction | 2025.09 | [Frontier Red Team](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Opus 4.6 | Anthropic | Zero-day discovery | 500+ novel vulns | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

#### Cyber Range / End-to-End Attack

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Network Attack | 37% | 2025.11 | [System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Cyber Range | All except 3 scenarios | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | Equifax Simulation | 2/5 autonomous | 2025.09 | [System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude | Anthropic | PicoCTF 2025 | Top 3% (297th/10,460) | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | HackTheBox AI vs Human | 30th/161, 19/20 solved | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

#### Cybersecurity Knowledge

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o1 | OpenAI | MC Cybersecurity Knowledge | 59% | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Grok 4 | xAI | WMDP-Cyber | 79% | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | WMDP-Cyber | 81.4% | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Sec-Gemini v1 | Google | CTI-MCQ | +11% over competitors | 2025.04 | [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

#### Prompt Injection / Robustness

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Operator (GPT-4o) | OpenAI | Prompt Injection | 99% recall | 2025.01 | [System Card](https://cdn.openai.com/operator_system_card.pdf) |
| Gemini 2.0 → 2.5 | Google | TAP Attack Success | 99.8% → 53.6% | 2025.05 | [Paper](https://arxiv.org/abs/2505.14534) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (coding) | 0% attack success | 2026.02 | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Grok 4 Fast | xAI | AgentDojo | 0–3% attack success | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |

#### Misuse / Behavioral

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Grok 4 Fast | xAI | AgentHarm | 8–10% completion | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4 | xAI | MASK (deception) | 0.43 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 | xAI | Sycophancy | 0.07 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |

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

---

## Benchmarks

### Security OF AI

> Protecting the AI model itself from attacks.

*TODO: Individual benchmark entries with detailed descriptions*

### Security BY AI

> AI performing cybersecurity tasks.

*TODO: Individual benchmark entries with detailed descriptions*

### Security FROM AI

> Assessing risks posed by AI to cybersecurity.

*TODO: Individual benchmark entries with detailed descriptions*

---

## Agents

> Cybersecurity AI agents (NOT general-purpose coding agents like Claude Code or Codex).

*TODO: Offensive agents, defensive agents, multi-purpose agents*

---

## Tools

> Evaluation frameworks and platforms for running cybersecurity benchmarks.

*TODO: Inspect, evaluation harnesses, CTF platforms*

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
