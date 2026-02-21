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

Detailed entries with performance data are in [`benchmarks/`](benchmarks/).

### Security OF AI

> Protecting the AI model itself from attacks.

**Vendor Benchmarks:**
- **Prompt Injection Eval** — Robustness to prompt injection attacks (OpenAI, Anthropic, Google)
- **[TAP](https://arxiv.org/abs/2312.02119)** — Tree of Attacks with Pruning jailbreak method (Google)
- **[AgentDojo](https://arxiv.org/abs/2406.13352)** — Prompt injection in agentic settings (xAI)
- **Jailbreak Robustness** — Universal jailbreak resistance testing (OpenAI, Anthropic)
- **[Automated Red Teaming (ART)](https://arxiv.org/abs/2505.14534)** — Continuous adversarial evaluation (Google)
- **Expert Red Teaming** — External expert adversarial testing (OpenAI, Anthropic, Google)

**Academic Benchmarks:**
- **[HarmBench](https://github.com/centerforaisafety/HarmBench)** — 510 behaviors, 18 attack methods, 33 LLMs (CAIS)
- **[JailbreakBench](https://github.com/JailbreakBench/jailbreakbench)** — 100 misuse behaviors with leaderboard (UPenn, ETH Zurich)
- **[StrongREJECT](https://github.com/alexandrasouly/strongreject)** — 313 forbidden prompts with rubric-based scoring (UC Berkeley)
- **[AdvBench / GCG](https://github.com/llm-attacks/llm-attacks)** — 520 harmful behaviors + gradient-based attack (CMU, Google DeepMind)
- **[PAIR](https://github.com/patrickrchao/JailbreakingLLMs)** — Black-box jailbreak in <20 queries (UPenn)
- **[AutoDAN](https://github.com/SheltonLiu-N/AutoDAN)** — Genetic algorithm stealthy jailbreaks (UW-Madison)
- **[SafetyBench](https://github.com/thu-coai/SafetyBench)** — 11,435 MCQs, 7 categories, EN/ZH (Tsinghua)
- **[SALAD-Bench](https://github.com/OpenSafetyLab/SALAD-BENCH)** — 21,000 questions, 66 categories (Peking U)
- **[TrustLLM](https://github.com/HowieHwong/TrustLLM)** — 30+ datasets, 6 trust dimensions (UIUC, Stanford, UCB)
- **[DecodingTrust](https://github.com/AI-secure/DecodingTrust)** — 8 trustworthiness dimensions (NeurIPS 2023 Outstanding Paper)
- **[CyberSecEval v1-v4](https://github.com/meta-llama/PurpleLlama)** — Insecure code gen, cyberattack compliance (Meta)

> Full details: [`benchmarks/security-of-ai/`](benchmarks/security-of-ai/)

### Security BY AI

> AI performing cybersecurity tasks.

**Offensive (CTF / Exploit / Pentest):**
- **[Cybench](https://cybench.github.io/)** — 40 professional CTF tasks (Anthropic)
- **[CyBench](https://cybench.github.io/)** — 40 CTF challenges via UK AISI Inspect (xAI)
- **[CyberGym](https://red.anthropic.com/2025/ai-for-cyber-defenders/)** — 1,507 CVEs in real OSS (Anthropic)
- **CVE-Bench** — Real-world web app CVE exploitation (OpenAI)
- **Cyber Range** — Multi-machine network attack scenarios (OpenAI, Anthropic)
- **[InterCode-CTF](https://arxiv.org/abs/2306.14898)** — 76 easy CTF challenges, saturated (Google)
- **[In-house CTF (GDM)](https://github.com/google-deepmind/dangerous-capability-evaluations)** — 13 medium challenges, open-sourced (Google)
- **Hack the Box** — Professional-level challenges (Google, Anthropic)
- **[NYU CTF Bench](https://github.com/NYU-LLM-CTF/NYU_CTF_Bench)** — 200 challenges, 6 categories (NYU)
- **[PrimeVul](https://github.com/DLVulDet/PrimeVul)** — 7K vulnerable + 229K benign functions, 140+ CWEs
- **[DiverseVul](https://github.com/wagner-group/diversevul)** — 18,945 vulnerable functions, 150 CWEs (UC Berkeley)
- **[SecLLMHolmes](https://github.com/ai4cloudops/SecLLMHolmes)** — GPT-4 achieves only 13% on real-world vuln detection (BU, IBM)

**Knowledge:**
- **[WMDP-Cyber](https://www.wmdp.ai/)** — Cyber killchain MC questions (xAI)
- **[SecBench](https://github.com/secbench-git/SecBench)** — 44,823 MCQs + 3,087 SAQs, 9 domains, EN/ZH
- **[CyberMetric](https://github.com/cybermetric/CyberMetric)** — 10,000 questions, 9 domains
- **[CTI-Bench](https://github.com/xashru/cti-bench)** — Threat intelligence tasks (RIT, NeurIPS 2024 Spotlight)
- **[SecQA](https://huggingface.co/datasets/zefang-liu/secqa)** — 242 concise cybersecurity MCQs
- **[CS-Eval](https://github.com/CS-EVAL/CS-Eval)** — 42 subcategories, 3 cognitive levels

**Defensive:**
- **Cybersecurity Investigation Benchmark** — 40 investigations, blind-ranked (Anthropic)
- **[CyberSOCEval](https://meta-llama.github.io/PurpleLlama/CyberSecEval/)** — SOC automation with CrowdStrike (Meta)
- **[AutoPatchBench](https://meta-llama.github.io/PurpleLlama/CyberSecEval/)** — Automated security patching (Meta)

> Full details: [`benchmarks/security-by-ai/`](benchmarks/security-by-ai/)

### Security FROM AI

> Assessing risks posed by AI to cybersecurity.

**Misuse / Dual-use:**
- **[AgentHarm](https://arxiv.org/abs/2410.09024)** — 110 malicious agent tasks (xAI, ICLR 2025)
- **Malware Benchmark** — Synthetic malware-related tasks (OpenAI)
- **Harmful Request Refusal** — Refusal rate on violative prompts (all 4 companies)
- **Zero-day Discovery Eval** — Model auditing OSS for novel vulns (Anthropic)
- **[CyberSecEval (Misuse)](https://github.com/meta-llama/PurpleLlama)** — 52% avg cyberattack compliance rate (Meta)
- **[WMDP](https://github.com/centerforaisafety/wmdp)** — 3,668 MCQs measuring hazardous knowledge (CAIS, ICML 2024)

**Behavioral / Alignment:**
- **[MASK](https://arxiv.org/abs/2406.11663)** — Deception measurement (xAI)
- **MakeMeSay** — Persuasion / manipulation eval (xAI)
- **Sycophancy Eval** — Ignoring own judgment for user agreement (xAI)
- **[Stealth / Situational Awareness](https://arxiv.org/abs/2505.01420)** — Oversight evasion + self-reasoning (Google)
- **[Sabotage Risk](https://alignment.anthropic.com/2025/sabotage-risk-report/)** — 9 sabotage pathways (Anthropic, METR-reviewed)

> Full details: [`benchmarks/security-from-ai/`](benchmarks/security-from-ai/)

---

## Agents

> Cybersecurity AI agents (NOT general-purpose coding agents like Claude Code or Codex).

### Offensive (21 agents)

| Agent | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[PentestGPT](https://github.com/GreyDGL/PentestGPT)** | NTU | Yes | LLM-powered pentest assistant (USENIX Security 2024) |
| **[ARTEMIS](https://github.com/Stanford-Trinity/ARTEMIS)** | Stanford / Gray Swan | Yes | Multi-agent pentest; 2nd in live enterprise test, beat 9/10 humans |
| **[CAI](https://github.com/aliasrobotics/cai)** | Alias Robotics | Yes | 300+ models, 3,600x over human pentesters on CTF benchmarks |
| **[XBOW](https://xbow.com/)** | XBOW | No | #1 on HackerOne leaderboard 2025; found vulns in Amazon, Disney, PayPal |
| **[D-CIPHER](https://github.com/NYU-LLM-CTF/nyuctf_agents)** | NYU | Yes | SOTA on NYU CTF (22.0%), Cybench (22.5%), HackTheBox (44.0%) |
| **[AutoPentester](https://github.com/YasodGinige/AutoPentester)** | Univ. Sydney | Yes | 27% better subtask completion, 39.5% more vuln coverage than PentestGPT |
| **[SWE-agent / EnIGMA](https://github.com/SWE-agent/SWE-agent)** | Princeton/NYU/TAU | Yes | 3.3x improvement on NYU CTF dataset (ICML 2025) |
| **[PentAGI](https://github.com/vxcontrol/pentagi)** | VXControl | Yes | 20+ built-in tools, sandboxed Docker, Neo4j knowledge graph |
| **[CRAKEN](https://github.com/NYU-LLM-CTF/nyuctf_agents_craken)** | NYU | Yes | Knowledge-based CTF agent; 25-30% more ATT&CK techniques |
| **[Reaper](https://github.com/ghostsecurity/reaper)** | Ghost Security | Yes | Agentic AI AppSec testing framework (Go, Apache 2.0) |
| **[Strix](https://github.com/usestrix/strix)** | usestrix | Yes | AI hackers with PoC validation, CI/CD via GitHub Actions |
| **[hackingBuddyGPT](https://github.com/ipa-lab/hackingBuddyGPT)** | TU Wien | Yes | LLM hacking research framework in 50 lines of code |
| **[PentestAgent](https://github.com/GH05TCREW/pentestagent)** | GH05TCREW | Yes | Black-box testing with attack playbooks, MCP extensibility |
| **[HackerGPT](https://github.com/Hacker-GPT/HackerGPT-2.0)** | Community | Yes | Ethical hacking assistant with Mixtral/Llama |
| **[ReaperAI](https://github.com/tac01337/ReaperAI)** | tac01337 | Yes | GPT-4 + RAG autonomous vuln exploitation on HTB |
| **[AutoAttacker](https://arxiv.org/abs/2403.01038)** | UC researchers | No | 14 attack types with RAG-augmented Metasploit |
| **[KryptoPilot](https://arxiv.org/abs/2601.09129)** | Academic | — | 100% InterCode-CTF, 56-60% NYU-CTF crypto |
| **[Penligent](https://penligent.ai/)** | Penligent | No | Multi-agent pentest with 120K+ CVE knowledge graph |
| **[TARS](https://github.com/osgil-defense/TARS)** | Osgil Defense | Yes | Orchestrator for Nmap, ZAP, RustScan, Nettacker |
| **[Auto-Pentest-GPT](https://github.com/Armur-Ai/Auto-Pentest-GPT-AI)** | Armur AI | Yes | Fine-tuned Mistral-7B with Kali Linux commands |
| **[CIPHER](https://www.researchgate.net/publication/385337738)** | Academic | — | LLM fine-tuned on 300+ pentesting writeups |

### Defensive (13 agents)

| Agent | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[Microsoft Security Copilot](https://www.microsoft.com/en-us/security/business/ai-machine-learning/microsoft-copilot-security)** | Microsoft | No | 37+ agents; Phishing Triage improves accuracy 77% |
| **[Charlotte AI](https://www.crowdstrike.com/en-us/platform/charlotte-ai/)** | CrowdStrike | No | >98% triage accuracy, Agentic SOAR, FedRAMP High |
| **[Cortex XSIAM / AgentiX](https://www.paloaltonetworks.com/cortex/cortex-xsiam)** | Palo Alto Networks | No | Trained on 1.2B playbooks; 98% MTTR reduction |
| **[Google TI Agentic](https://gtidocs.virustotal.com/docs/agentic-platform)** | Google | No | Mandiant + VirusTotal data; GA for Enterprise |
| **[Sec-Gemini v1](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html)** | Google | No | Specialized CTI model; +11% on CTI-MCQ |
| **[Big Sleep](https://projectzero.google/2024/10/from-naptime-to-big-sleep.html)** | Google P0 + DeepMind | No | First AI-discovered real-world zero-day (SQLite) |
| **[OpenAI Aardvark](https://openai.com/index/strengthening-cyber-resilience/)** | OpenAI | No | Agentic security researcher (private beta) |
| **[Project Ire](https://www.microsoft.com/en-us/research/blog/project-ire-autonomously-identifies-malware-at-scale/)** | Microsoft Research | No | Autonomous malware RE; precision 0.98; Black Hat 2025 |
| **[Dropzone AI](https://www.dropzone.ai)** | Dropzone AI | No | AI SOC analyst; 3-10 min vs 30-40 min manual |
| **[Exaforce](https://www.exaforce.com)** | Exaforce | No | Full-lifecycle AI SOC; $75M Series A (Khosla) |
| **[Radiant Security](https://radiantsecurity.ai)** | Radiant Security | No | Agentic triage/investigation/response with root cause |
| **[Simbian AI](https://simbian.ai)** | Simbian | No | 4 autonomous agents; #1 AI SOC ARR |
| **[Joe Reverser](https://www.joesecurity.org/joe-reverser)** | Joe Security | No | Agentic malware/phishing analyst with MITRE ATT&CK |

### Multi-Purpose (4 agents)

| Agent | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[Fabric](https://github.com/danielmiessler/fabric)** | Daniel Miessler | Yes | 200+ prompt patterns for cybersecurity tasks |
| **[Floki / Dapr Agents](https://github.com/Cyb3rWard0g/floki)** | Cyb3rWard0g | Yes | Multi-agent framework; donated to CNCF Dapr project |
| **[BurpGPT](https://github.com/aress31/burpgpt)** | aress31 | Yes | Burp Suite + LLM passive scanning extension |
| **[Burp AI Agent](https://github.com/six2dez/burp-ai-agent)** | six2dez | Yes | 7 AI backends, 53+ MCP tools, 62 vuln classes |

> Full details: [`agents/`](agents/)

---

## Tools

> Evaluation frameworks, platforms, and tools for running cybersecurity AI benchmarks.

### Evaluation Frameworks

| Tool | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)** | UK AISI | Yes | Python framework for reproducible LLM evaluations with sandboxing |
| **[Inspect Cyber](https://inspect.cyber.aisi.org.uk/)** | UK AISI | Yes | Specialized cyber eval extension with CTF/cyber range YAML configs |
| **[Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals)** | UK AISI + community | Yes | Collection of cyber evals (Cybench, WMDP, AgentHarm, etc.) |
| **[Vivaria](https://github.com/METR/vivaria)** | METR | Yes | Agent evaluation platform (transitioning to Inspect) |
| **[Dangerous Capability Evals](https://github.com/google-deepmind/dangerous-capability-evaluations)** | Google DeepMind | Partial | Frontier model evaluation with CCL thresholds |
| **[lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness)** | EleutherAI | Yes | Unified LLM eval framework (includes WMDP-Cyber) |

### Benchmark Suites

| Tool | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[PurpleLlama / CyberSecEval](https://github.com/meta-llama/PurpleLlama)** | Meta | Yes | Insecure code gen, cyberattack compliance, SOC eval, auto-patching (v1-v4) |
| **[CAIBench](https://arxiv.org/abs/2510.24317)** | Alias Robotics | Yes | Meta-benchmark: 5 categories, 10,000+ instances |
| **[ExCyTIn-Bench](https://github.com/microsoft/SecRL)** | Microsoft | Yes | SOC threat investigation with 589 Q&A pairs from Sentinel |
| **[eyeballvul](https://github.com/timothee-chauvin/eyeballvul)** | METR-affiliated | Yes | 24,000+ real vulnerabilities, updated weekly |

### Red Team / Adversarial Testing

| Tool | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[HarmBench](https://github.com/centerforaisafety/HarmBench)** | CAIS | Yes | Standardized red teaming: 18 attacks vs 33 LLMs |
| **[StrongREJECT](https://github.com/dsbowen/strong_reject)** | UC Berkeley / GDM | Yes | Jailbreak eval with SOTA human agreement |
| **[JailbreakBench](https://github.com/JailbreakBench/jailbreakbench)** | Multi-institution | Yes | 100 behaviors + attack/defense leaderboard |
| **[Garak](https://github.com/NVIDIA/garak)** | NVIDIA | Yes | LLM vulnerability scanner (prompt injection, jailbreak, data leakage) |
| **[Promptfoo](https://github.com/promptfoo/promptfoo)** | Open source | Yes | LLM red teaming CLI with OWASP Top 10 + CI/CD |

### CTF Platforms

| Platform | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[CTFd](https://github.com/CTFd/CTFd)** | CTFd LLC | Yes | Most widely used CTF hosting framework |
| **[picoCTF](https://picoctf.org/)** | CMU CyLab | Free | 800,000+ users; Claude ranked top 3% in 2025 |
| **[Hack The Box](https://www.hackthebox.com/)** | HTB | No | AI Range (Dec 2025) for autonomous agent benchmarking |

### Simulation Environments

| Tool | Created by | Open Source | Summary |
|---|---|:---:|---|
| **[CyberBattleSim](https://github.com/microsoft/CyberBattleSim)** | Microsoft Research | Yes | OpenAI Gym environment for RL attack/defense |
| **[ControlArena](https://control-arena.aisi.org.uk/)** | UK AISI + Redwood | Yes | AI control experiments for misalignment prevention |

> Full details: [`tools/`](tools/)

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
