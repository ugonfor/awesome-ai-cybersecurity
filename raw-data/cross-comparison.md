# Cross-Comparison: AI Cybersecurity Benchmarks Across Vendors

## 1. Risk Framework Comparison

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **Framework** | Preparedness Framework (v2) | Responsible Scaling Policy (RSP v2.2) | Frontier Safety Framework (FSF v3.0) | Risk Management Framework |
| **Risk Levels** | Low → Medium → High → Critical | ASL-1 → ASL-2 → ASL-3 → ASL-4 | CCL alert threshold → CCL reached | Abuse / Propensities / Dual-use |
| **Cyber Threshold Definition** | High: automate end-to-end ops against hardened targets OR automate zero-day discovery/exploitation | ASL-3: success ≥1/5 times in ≥2/6 classes of expert vuln discovery & exploit dev | Cyber Uplift L1: significantly assist high-impact attacks with ≥10x cost reduction | Not explicitly defined as threshold |
| **First Threshold Crossed** | GPT-5.3-Codex (Feb 2026) — **HIGH** | Claude Opus 4 (May 2025) — **ASL-3** | None crossed (alert only) | None crossed |
| **Third-party Testing** | US/UK AISI | US/UK AISI, METR | — | UK AISI |
| **Framework URL** | [PDF](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf) | [Web](https://www.anthropic.com/responsible-scaling-policy) | [PDF](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf) | [PDF](https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf) |

---

## 2. Benchmark Cross-Comparison (Which Company Uses What)

### Security BY AI — Offensive (Cyber Capability)

| Benchmark | OpenAI | Anthropic | Google | xAI | Category | Description |
|---|:---:|:---:|:---:|:---:|---|---|
| **CTF (internal/custom)** | ✅ | ✅ | ✅ | — | BY-AI / Offensive | Each company's proprietary CTF challenge sets |
| **[Cybench](https://cybench.github.io/)** | — | ✅ | — | ✅ | BY-AI / Offensive | 40 professional CTF tasks from 4 competitions (xAI spells it "CyBench" — same benchmark) |
| **CyberGym** | — | ✅ | — | — | BY-AI / Offensive | Real-world vuln detection in open-source software |
| **CVE-Bench** | ✅ | — | — | — | BY-AI / Offensive | Exploit real-world web app CVEs (pass@1) |
| **Cyber Range** | ✅ | ✅ | — | — | BY-AI / Offensive | Multi-machine network attack scenarios |
| **InterCode-CTF** | — | — | ✅ | — | BY-AI / Offensive | 76 easy CTF challenges (saturated) |
| **In-house CTF (GDM)** | — | — | ✅ | — | BY-AI / Offensive | 13 medium challenges (open-sourced via UK AISI Inspect) |
| **Hack the Box** | — | ✅ | ✅ | — | BY-AI / Offensive | Professional-level CTF challenges |
| **Key Skills Benchmark** | — | — | ✅ | — | BY-AI / Offensive | Recon, tool dev, OPSEC (MITRE ATT&CK aligned) |
| **Pattern Labs External CTFs** | — | — | ✅ | — | BY-AI / Offensive | 50 non-public challenges (anti-contamination) |
| **PicoCTF / HTB / WRCCDC** | — | ✅ | — | — | BY-AI / Offensive | Real competitive CTF events |
| **Equifax Simulation** | — | ✅ | — | — | BY-AI / Offensive | High-fidelity breach simulation |
| **CMU Cyber Ranges** | — | ✅ | — | — | BY-AI / Offensive | ~50-host network simulations |

### Security BY AI — Knowledge

| Benchmark | OpenAI | Anthropic | Google | xAI | Category | Description |
|---|:---:|:---:|:---:|:---:|---|---|
| **WMDP-Cyber** | — | — | — | ✅ | BY-AI / Knowledge | Cyber killchain MC questions |
| **MC Cybersecurity Knowledge** | ✅ | — | — | — | BY-AI / Knowledge | OpenAI internal MC eval |
| **CTI-MCQ** | — | — | ✅ | — | BY-AI / Knowledge | Threat intelligence knowledge (from [CTI-Bench](https://github.com/xashru/cti-bench), used by Sec-Gemini) |
| **CTI-RCM** | — | — | ✅ | — | BY-AI / Knowledge | Root cause → CWE mapping (from [CTI-Bench](https://github.com/xashru/cti-bench), used by Sec-Gemini) |

### Security OF AI — Jailbreak / Prompt Injection / Robustness

| Benchmark | OpenAI | Anthropic | Google | xAI | Category | Description |
|---|:---:|:---:|:---:|:---:|---|---|
| **Prompt Injection Eval** | ✅ | ✅ | ✅ | — | OF-AI / Robustness | Model robustness to prompt injection attacks |
| **TAP Attack Success Rate** | — | — | ✅ | — | OF-AI / Robustness | Tree of Attacks with Pruning (99.8% → 53.6%) |
| **AgentDojo** | — | — | — | ✅ | OF-AI / Robustness | Prompt injection in agentic settings |
| **Jailbreak Robustness** | ✅ | ✅ | — | — | OF-AI / Jailbreak | Universal jailbreak resistance testing |
| **Automated Red Teaming (ART)** | — | — | ✅ | — | OF-AI / Red Team | Continuous adversarial evaluation framework |
| **Expert Red Teaming** | ✅ | ✅ | ✅ | — | OF-AI / Red Team | External experts adversarially testing models |

### Security FROM AI — Misuse Risk / Dual-use

| Benchmark | OpenAI | Anthropic | Google | xAI | Category | Description |
|---|:---:|:---:|:---:|:---:|---|---|
| **AgentHarm** | — | — | — | ✅ | FROM-AI / Misuse | Malicious agentic task completion (fraud, cybercrime) |
| **Malware Benchmark** | ✅ | — | — | — | FROM-AI / Misuse | Synthetic malware-related task eval (Codex) |
| **Harmful Request Refusal** | ✅ | ✅ | ✅ | ✅ | FROM-AI / Safety | Refusal rate on violative/harmful prompts |
| **Input/Output Filters** | — | — | — | ✅ | FROM-AI / Safety | False negative rates for restricted content |
| **Zero-day Discovery Eval** | — | ✅ | — | — | FROM-AI / Risk | Model auditing open-source code for novel vulns |

### Security FROM AI — Behavioral / Alignment

| Benchmark | OpenAI | Anthropic | Google | xAI | Category | Description |
|---|:---:|:---:|:---:|:---:|---|---|
| **MASK** | — | — | — | ✅ | FROM-AI / Alignment | Deception measurement under pressure |
| **MakeMeSay** | — | — | — | ✅ | FROM-AI / Alignment | Persuasion / manipulation eval |
| **Sycophancy Eval** | — | — | — | ✅ | FROM-AI / Alignment | Ignoring own judgment for user agreement |
| **Stealth Eval** | — | — | ✅ | — | FROM-AI / Alignment | Ability to circumvent oversight |
| **Situational Awareness** | — | — | ✅ | — | FROM-AI / Alignment | Self/environment reasoning |
| **Sabotage Risk** | — | ✅ | — | — | FROM-AI / Alignment | 9 sabotage pathways (METR-reviewed) |

---

## 2.5. Reported Performance Numbers by Benchmark

### CTF Performance (Professional-level, comparable difficulty)

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-4o | OpenAI | Custom CTF (Professional) | 1% | 2024.08 | [GPT-4o System Card](https://cdn.openai.com/gpt-4o-system-card.pdf) |
| o1-preview | OpenAI | Custom CTF (Professional) | 2.5% | 2024.09 | [o1 System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1-mini | OpenAI | Custom CTF (Professional) | 3.9% | 2024.09 | [o1 System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1 | OpenAI | Custom CTF (Professional) | 13% | 2024.12 | [o1 System Card](https://cdn.openai.com/o1-system-card-20241205.pdf) |
| Deep Research (no browse) | OpenAI | Custom CTF (Professional) | 47% | 2025.02 | [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| Deep Research (w/ browse) | OpenAI | Custom CTF (Professional) | 70% | 2025.02 | [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| o3 | OpenAI | Custom CTF (Professional) | ~58% | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| GPT-5 | OpenAI | Custom CTF (Professional, pass@12) | ~27% | 2025.08 | [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Custom CTF (Professional) | ~76% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Custom CTF (Professional) | All passed | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude 3.7 Sonnet | Anthropic | Cybench (40 tasks) | 35.9% | 2025.02 | [Claude 3.7 Sonnet System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
| Claude Opus 4 | Anthropic | Custom CTF (easy/med/hard) | 11/11 easy, 1/2 med, 0/2 hard | 2025.05 | [Claude 4 System Card](https://www.anthropic.com/claude-4-system-card) |
| Claude Sonnet 4.5 | Anthropic | Cybench (40 tasks) | 76.5% | 2025.09 | [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.6 | Anthropic | 40 cyber investigations | 38/40 best (blind-ranked) | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 2.5 Deep Think | Google | InterCode-CTF (Easy, 76 tasks) | 73/76 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | In-house CTF (Medium, 13 tasks) | 13/13 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | Hack the Box (Hard) | 3/13 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.0 Flash | Google | Pattern Labs External CTF (50 tasks) | 11/50 | 2025.04 | [Gemini 2.0 Flash Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf) |
| Gemini 3 Pro | Google | Hack the Box (Hard) | 11/12 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |

### CVE / Vulnerability Benchmarks

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.2-Codex | OpenAI | CVE-Bench (pass@1) | 87% | 2025.12 | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| Claude Sonnet 4.5 | Anthropic | CyberGym ($2 cost) | 28.9% | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials, no cost limit) | 66.7% vuln reproduction | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym — new vuln discovery (30 trials) | 33%+ | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Opus 4.6 | Anthropic | CyberGym (1,507 CVEs) | 500+ zero-days found in pre-release | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |

### Cyber Range / End-to-End Attack Performance

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Network Attack | 37% avg success | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Vuln Discovery | 41% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Evasion | 43% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Cyber Range | All except 3 scenarios | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | Equifax Simulation | 2/5 trials autonomous | 2025.09 | [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude | Anthropic | PicoCTF 2025 | 297th/10,460 (top 3%), 32/41 | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | HackTheBox AI vs Human | 30th/161, 19/20 challenges | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | WRCCDC | 6th/9 teams | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

### Cybersecurity Knowledge (MC / Knowledge Benchmarks)

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o3-mini | OpenAI | MC Cybersecurity Knowledge | 53% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| o1 | OpenAI | MC Cybersecurity Knowledge | 59% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Grok 4 | xAI | WMDP-Cyber | 79% | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | WMDP-Cyber | 81.4% | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Sec-Gemini v1 | Google | CTI-MCQ | +11% over competitors | 2025.04 | [Sec-Gemini Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |
| Sec-Gemini v1 | Google | CTI-RCM | +10.5% over competitors | 2025.04 | [Sec-Gemini Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

### Security OF AI — Prompt Injection / Robustness

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Operator (GPT-4o) | OpenAI | Prompt Injection Eval | 99% recall (77 attempts) | 2025.01 | [Operator System Card](https://cdn.openai.com/operator_system_card.pdf) |
| Gemini 2.0 | Google | TAP Attack Success Rate | 99.8% (vulnerable) | 2025.05 | [Prompt Injection Paper](https://arxiv.org/abs/2505.14534) |
| Gemini 2.5 | Google | TAP Attack Success Rate | 53.6% (improved) | 2025.05 | [Prompt Injection Paper](https://arxiv.org/abs/2505.14534) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (coding + ext. thinking) | 0% attack success | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (browser) | <0.3% attack success | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Grok 4 Fast | xAI | AgentDojo (attack success rate) | 0–3% | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |

### Security FROM AI — Misuse / Behavioral

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Grok 4 | xAI | AgentHarm (malicious task completion) | — | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | AgentHarm | 8–10% | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | AgentHarm (agentic) | <14% | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4 | xAI | MASK (deception) | 0.43 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4.1 Thinking | xAI | MASK (deception) | 0.49 | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4 | xAI | Sycophancy Eval | 0.07 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4.1 Thinking | xAI | Sycophancy Eval | 0.19 | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 | xAI | MakeMeSay (attacker success) | 0% | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

## 3. Benchmark Overlap Matrix (Shared vs Proprietary)

| Status | Benchmarks |
|---|---|
| **Used by 4 companies** | Harmful Request Refusal (each with internal version) |
| **Used by 3 companies** | Expert Red Teaming (OpenAI, Anthropic, Google), Prompt Injection Eval (OpenAI, Anthropic, Google) |
| **Used by 2 companies** | Cyber Range (OpenAI, Anthropic), Jailbreak Robustness (OpenAI, Anthropic) |
| **Used by 1 company** | CVE-Bench (OpenAI only), CyberGym (Anthropic only), InterCode-CTF (Google only), WMDP-Cyber (xAI only), AgentHarm (xAI only), CTI-MCQ/RCM (Google/Sec-Gemini only) |

### Key Insight: Almost No Shared Quantitative Benchmarks

Despite all 4 companies evaluating cybersecurity, **there is virtually no overlap in quantitative benchmarks**. Each company has developed or adopted its own unique set:

- **OpenAI**: CTF (custom) + CVE-Bench + Cyber Range
- **Anthropic**: Cybench + CyberGym + CMU Cyber Range + real CTF competitions
- **Google**: InterCode-CTF + In-house CTF + HTB + Key Skills + Pattern Labs
- **xAI**: Cybench (spelled "CyBench") + WMDP-Cyber + AgentHarm + AgentDojo

This makes **direct cross-company comparison nearly impossible** — which is exactly the problem this awesome repo aims to solve.

---

## 4. Documentation Maturity Comparison

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **First cyber-specific benchmark** | GPT-4o (Aug 2024) | Claude 3 (Mar 2024) | Phuong et al. (Mar 2024) | Grok 4 (Aug 2025) |
| **Total documents w/ cyber benchmarks** | 19 | 24 | 25+ | 9 |
| **System card page count (latest)** | ~50-80p | 213p (Opus 4.6) | ~30-50p | ~20-30p |
| **Open-sources evals?** | No | No | Yes (In-house CTF via Inspect) | No (uses UK AISI Inspect) |
| **Real-world threat intel published?** | No | Yes (GTG-1002 espionage) | Yes (12,000+ incidents via GTI) | No |
| **Specialized cyber model?** | Aardvark (private beta) | — | Sec-Gemini v1 | — |

---

## 5. Timeline: Cyber Risk Level Progression (All Companies)

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
| 2025.08 | GPT-5: Below High | — | Gemini 2.5 Deep Think: CCL alert | Grok 4: below human pro |
| 2025.11 | GPT-5.1: Below High | Opus 4.5: ASL-3 | Gemini 3 Pro: CCL alert, not met | Grok 4.1: below human pro |
| 2026.02 | GPT-5.3: **HIGH** | Opus 4.6: ASL-3 | Gemini 3.1 Pro: CCL alert, not met | — |

---

## 6. Sources

### OpenAI
- [Preparedness Framework v2](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf)
- [GPT-4 System Card](https://cdn.openai.com/papers/gpt-4-system-card.pdf)
- [GPT-4o System Card](https://cdn.openai.com/gpt-4o-system-card.pdf)
- [o1 System Card (Dec 2024)](https://cdn.openai.com/o1-system-card-20241205.pdf)
- [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf)
- [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf)
- [GPT-4.5 System Card](https://cdn.openai.com/gpt-4-5-system-card-2272025.pdf)
- [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf)
- [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf)
- [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf)
- [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf)
- [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf)
- [Strengthening Cyber Resilience](https://openai.com/index/strengthening-cyber-resilience/)

### Anthropic
- [RSP v2.2](https://www.anthropic.com/responsible-scaling-policy)
- [Claude 3 Model Card](https://www-cdn.anthropic.com/c6a80a657af445f40e31afac050f3bf76d3b1404.pdf)
- [Claude 3.7 Sonnet System Card](https://anthropic.com/claude-3-7-sonnet-system-card)
- [Claude Opus 4 System Card](https://www.anthropic.com/claude-4-system-card)
- [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card)
- [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card)
- [ASL-3 Deployment Safeguards](https://www.anthropic.com/asl3-deployment-safeguards)
- [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/)
- [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/)
- [Disrupting AI Espionage](https://www.anthropic.com/news/disrupting-AI-espionage)

### Google
- [FSF v3.0](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf)
- [Gemini 2.5 Technical Report](https://arxiv.org/abs/2507.06261)
- [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf)
- [Phuong et al. 2024 — Dangerous Capabilities](https://arxiv.org/abs/2403.13793)
- [Defending Gemini Against Prompt Injections](https://arxiv.org/abs/2505.14534)
- [Sec-Gemini v1](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html)
- [Model Cards Index](https://deepmind.google/models/model-cards/)

### xAI
- [Risk Management Framework](https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf)
- [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf)
- [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf)
- [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf)
- [FAIF](https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf)
- [xAI Safety](https://x.ai/safety)

### Third-party
- [US/UK AISI Joint Test — o1](https://www.nist.gov/system/files/documents/2024/12/18/US_UK_AI%20Safety%20Institute_%20December_Publication-OpenAIo1.pdf)
- [Framework for Evaluating Emerging Cyberattack Capabilities](https://arxiv.org/abs/2503.11917)
