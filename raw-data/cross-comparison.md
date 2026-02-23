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

## 2. AI4Security — Offensive Capability

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **CTF (internal/custom)** | ✅ | ✅ | ✅ | — | Each company's proprietary CTF challenge sets |
| **[Cybench](https://cybench.github.io/)** | — | ✅ | — | ✅ | 40 professional CTF tasks from 4 competitions (xAI spells it "CyBench" — same benchmark) |
| **CyberGym** | — | ✅ | — | — | Real-world vuln detection in open-source software (1,507 CVEs; created by UC Berkeley RDI) |
| **CVE-Bench** | ✅ | — | — | — | Exploit real-world web app CVEs (pass@1) |
| **OpenAI Cyber Range** | ✅ | — | — | — | 15 multi-machine network attack scenarios (internal) |
| **CMU Cyber Ranges / Incalmo** | — | ✅ | — | — | ~50-host networks + Equifax breach simulation (CMU CyLab + Incalmo) |
| **InterCode-CTF** | — | — | ✅ | — | 76 easy CTF challenges (saturated) |
| **In-house CTF (GDM)** | — | — | ✅ | — | 13 medium challenges (open-sourced via UK AISI Inspect) |
| **Hack the Box** | — | ✅ | ✅ | — | Professional-level CTF challenges |
| **Key Skills Benchmark** | — | — | ✅ | — | Recon, tool dev, OPSEC (MITRE ATT&CK aligned) |
| **Pattern Labs External CTFs** | — | — | ✅ | — | 50 non-public challenges (anti-contamination) |
| **PicoCTF / HTB / WRCCDC** | — | ✅ | — | — | Real competitive CTF events |
| **Equifax Simulation** | — | ✅ | — | — | High-fidelity breach simulation |

### Performance Scores

#### CTF Performance

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-4o | OpenAI | Custom CTF (Professional) | 1% | 2024.08 | [GPT-4o System Card](https://cdn.openai.com/gpt-4o-system-card.pdf) |
| o1-preview | OpenAI | Custom CTF (Professional) | 2.5% | 2024.09 | [o1 System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1-mini | OpenAI | Custom CTF (Professional) | 3.9% | 2024.09 | [o1 System Card](https://cdn.openai.com/o1-system-card.pdf) |
| o1 | OpenAI | Custom CTF (Professional) | 13% | 2024.12 | [o1 System Card](https://cdn.openai.com/o1-system-card-20241205.pdf) |
| o3-mini | OpenAI | Custom CTF (HS / Collegiate) | 61% / 21% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Deep Research (no browse) | OpenAI | Custom CTF (Professional) | 47% | 2025.02 | [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| Deep Research (w/ browse) | OpenAI | Custom CTF (Professional) | 70% | 2025.02 | [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf) |
| o3 | OpenAI | Custom CTF (Professional, pass@12) | ~59% | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| o4-mini | OpenAI | Custom CTF (Professional, pass@12) | ~41% | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| GPT-5 | OpenAI | Custom CTF (Professional, pass@12) | ~27% | 2025.08 | [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Custom CTF (Professional) | ~76% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.2-Codex | OpenAI | Custom CTF (Professional) | Strongest at time | 2025.12 | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| GPT-5.3-Codex | OpenAI | Custom CTF (Professional) | All passed | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude 3.7 Sonnet | Anthropic | Cybench (40 tasks) | 35.9% (pass@5) | 2025.02 | [Claude 3.7 Sonnet System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
| Claude Opus 4 | Anthropic | Custom CTF (easy/med/hard) | 11/11 easy, 1/2 med, 0/2 hard | 2025.05 | [Claude 4 System Card](https://www.anthropic.com/claude-4-system-card) |
| Claude Sonnet 4.5 | Anthropic | Cybench (40 tasks) | 76.5% (pass@10) | 2025.09 | [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.5 | Anthropic | Cybench | 82% pass@1 | 2025.11 | [Claude Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Opus 4.6 | Anthropic | Cybench (37 tasks) | 93% pass@1 | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 2.5 Deep Think | Google | InterCode-CTF (Easy, 76 tasks) | 73/76 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | In-house CTF (Medium, 13 tasks) | 13/13 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | Hack the Box (Hard) | 3/13 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.0 Flash | Google | Pattern Labs External CTF (50 tasks) | 11/50 | 2025.04 | [Gemini 2.0 Flash Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf) |
| Gemini 3 Pro | Google | Key Skills v1 (Hard) | 11/12 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
| Gemini 3 Pro | Google | Key Skills v2 (End-to-end) | 0/13 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
| Gemini 3.1 Pro | Google | FSF Cyber Evals (Deep Think) | Increased vs 3 Pro | 2026.02 | [Gemini 3.1 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf) |
| Grok 4 | xAI | Cybench (40 tasks) | 43% unguided | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | Cybench (40 tasks) | 30% unguided | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | Cybench (40 tasks) | 39% unguided | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

#### CVE / Vulnerability Discovery

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5.2-Codex | OpenAI | CVE-Bench (pass@1) | 87% | 2025.12 | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| GPT-5.3-Codex | OpenAI | CVE-Bench (pass@1) | 90% (34/40 challenges) | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | CyberGym ($2 cost limit) | 28.9% SOTA | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials) | 66.7% vuln reproduction | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials, new vulns) | 33%+ new vuln discovery | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Opus 4.5 | Anthropic | CyberGym (pass@1) | 50.63% | 2025.11 | [Claude Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Sonnet 4.6 | Anthropic | CyberGym (pass@1) | 65.2% | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | Anthropic | Zero-day Discovery | 500+ zero-days in pre-release testing | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |

#### End-to-End Attack / Cyber Range

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o3 | OpenAI | Cyber Range | 0% (2 scenarios, unaided) | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| o4-mini | OpenAI | Cyber Range | 0% (2 scenarios, unaided) | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Network Attack | 37% avg success | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Vuln Discovery | 41% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Cyber Range — Evasion | 43% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.3-Codex | OpenAI | Cyber Range | 80% (12/15 scenarios) | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | Equifax Simulation | 2/5 trials autonomous | 2025.09 | [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |

#### Real-World Competitions

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Claude | Anthropic | PicoCTF 2025 | 297th/10,460 (top 3%), 32/41 challenges | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | HackTheBox AI vs Human | 30th/161 overall, 4th/8 AI teams, 19/20 challenges | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | WRCCDC Regional | 6th/9 teams | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | WRCCDC Qualifier | 10th/28 teams | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | Airbnb Competition | 39th/~180 teams, 15/30 challenges | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | PlaidCTF | 0 challenges solved | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | DEF CON CTF Qualifier | 0 challenges solved | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

---

## 3. AI4Security — Defensive Capability

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **Cybersecurity Investigation (Anthropic)** | — | ✅ | — | — | 40 real-world cyber investigations blind-ranked by expert analysts |
| **WRCCDC (Defensive Competition)** | — | ✅ | — | — | Real defensive competition (qualifying + regional) |
| **CyberSOCEval (Meta/CrowdStrike)** | — | — | — | — | SOC analyst task evaluation (not used by big 4, but notable) |

### Performance Scores

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Claude Opus 4.6 | Anthropic | 40 cyber investigations | 38/40 best (blind-ranked) | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude | Anthropic | WRCCDC Qualifier | 10th/28 teams | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | WRCCDC Regional | 6th/9 teams | 2025 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

---

## 4. AI4Security — Cyber Knowledge

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **WMDP-Cyber** | — | — | — | ✅ | Cyber killchain MC questions (recon, weaponization, exploitation, post-exploitation) |
| **MC Cybersecurity Knowledge** | ✅ | — | — | — | OpenAI internal MC eval |
| **CTI-MCQ** | — | — | ✅ | — | Threat intelligence knowledge (from [CTI-Bench](https://github.com/xashru/cti-bench) by Rochester IT, used by Sec-Gemini) |
| **CTI-RCM** | — | — | ✅ | — | Root cause → CWE mapping (from [CTI-Bench](https://github.com/xashru/cti-bench) by Rochester IT, used by Sec-Gemini) |

### Performance Scores

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o3-mini | OpenAI | MC Cybersecurity Knowledge | 53% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| o1 | OpenAI | MC Cybersecurity Knowledge | 59% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Grok 4 | xAI | WMDP-Cyber | 79% | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | WMDP-Cyber | 81.4% | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | WMDP-Cyber | 84% | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Sec-Gemini v1 | Google | CTI-MCQ | +11% over competitors | 2025.04 | [Sec-Gemini Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |
| Sec-Gemini v1 | Google | CTI-RCM | +10.5% over competitors | 2025.04 | [Sec-Gemini Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

---

## 5. Security4AI — Model Robustness

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **Prompt Injection Eval** | ✅ | ✅ | ✅ | — | Model robustness to prompt injection attacks |
| **TAP Attack Success Rate** | — | — | ✅ | — | Tree of Attacks with Pruning |
| **AgentDojo** | — | — | — | ✅ | Prompt injection in agentic settings |
| **Jailbreak Robustness** | ✅ | ✅ | — | — | Universal jailbreak resistance testing |
| **Automated Red Teaming (ART)** | — | — | ✅ | — | Continuous adversarial evaluation framework |
| **Expert Red Teaming** | ✅ | ✅ | ✅ | — | External experts adversarially testing models |

### Performance Scores

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Operator (GPT-4o) | OpenAI | Prompt Injection Eval | 99% recall (77 attempts) | 2025.01 | [Operator System Card](https://cdn.openai.com/operator_system_card.pdf) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (coding + ext. thinking) | 0% attack success | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.6 | Anthropic | Prompt Injection (browser) | <0.3% attack success | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Gemini 2.0 | Google | TAP Attack Success Rate | 99.8% (vulnerable) | 2025.05 | [Prompt Injection Paper](https://arxiv.org/abs/2505.14534) |
| Gemini 2.5 | Google | TAP Attack Success Rate | 53.6% (improved) | 2025.05 | [Prompt Injection Paper](https://arxiv.org/abs/2505.14534) |
| Grok 4 | xAI | AgentDojo (attack success rate) | 0.02 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | AgentDojo (attack success rate) | 0.00–0.03 | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | AgentDojo (attack success rate) | 0.05 (T) / 0.01 (NT) | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

## 6. Security4AI — Misuse Risk & Alignment

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **AgentHarm** | — | — | — | ✅ | Malicious agentic task completion (EPFL, Gray Swan, UK AISI, Oxford, CMU) |
| **Malware Benchmark** | ✅ | — | — | — | Synthetic malware-related task eval (Codex) |
| **Harmful Request Refusal** | ✅ | ✅ | ✅ | ✅ | Refusal rate on violative/harmful prompts |
| **Input/Output Filters** | — | — | — | ✅ | False negative rates for restricted content |
| **Zero-day Discovery Eval** | — | ✅ | — | — | Model auditing open-source code for novel vulns |
| **MASK** | — | — | — | ✅ | Deception measurement under pressure (CAIS, [arxiv:2503.03750](https://arxiv.org/abs/2503.03750)) |
| **MakeMeSay** | — | — | — | ✅ | Persuasion / manipulation eval (OpenAI / Google DeepMind) |
| **Sycophancy Eval** | — | — | — | ✅ | Ignoring own judgment for user agreement |
| **Stealth Eval** | — | — | ✅ | — | Ability to circumvent oversight |
| **Situational Awareness** | — | — | ✅ | — | Self/environment reasoning |
| **Sabotage Risk** | — | ✅ | — | — | 9 sabotage pathways (METR-reviewed) |

### Performance Scores

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Operator (GPT-4o) | OpenAI | Harmful Task Refusal | 97% | 2025.01 | [Operator System Card](https://cdn.openai.com/operator_system_card.pdf) |
| Grok 4 | xAI | AgentHarm (malicious task completion) | 0.14 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | AgentHarm | 0.08 / 0.10 | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | AgentHarm | 0.14 (T) / 0.04 (NT) | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4 | xAI | MASK (deception) | 0.43 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | MASK (deception) | 0.47 / 0.63 | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | MASK (deception) | 0.49 / 0.46 | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4 | xAI | Sycophancy Eval | 0.07 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | Sycophancy Eval | 0.10 / 0.13 | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | Sycophancy Eval | 0.19 / 0.23 | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4 | xAI | MakeMeSay (attacker success) | 0.12 | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | MakeMeSay (attacker success) | 0.12 | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | MakeMeSay (attacker success) | 0% | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

## 7. Benchmark Overlap Summary

| Status | Benchmarks |
|---|---|
| **Used by 4 companies** | Harmful Request Refusal (each with internal version) |
| **Used by 3 companies** | Expert Red Teaming (OpenAI, Anthropic, Google), Prompt Injection Eval (OpenAI, Anthropic, Google) |
| **Used by 2 companies** | Cybench (Anthropic, xAI), Hack the Box (Anthropic, Google), Jailbreak Robustness (OpenAI, Anthropic) |
| **Used by 1 company** | CVE-Bench (OpenAI only), CyberGym (Anthropic only), InterCode-CTF (Google only), WMDP-Cyber (xAI only), AgentHarm (xAI only), AgentDojo (xAI only), CTI-MCQ/RCM (Google/Sec-Gemini only), MASK (xAI only), MakeMeSay (xAI only) |

### Key Insight: Almost No Shared Quantitative Benchmarks

Despite all 4 companies evaluating cybersecurity, **there is virtually no overlap in quantitative benchmarks**. Each company has developed or adopted its own unique set:

- **OpenAI**: CTF (custom) + CVE-Bench + OpenAI Cyber Range
- **Anthropic**: Cybench + CyberGym + CMU Cyber Range + real CTF competitions
- **Google**: InterCode-CTF + In-house CTF + HTB + Key Skills + Pattern Labs
- **xAI**: Cybench (spelled "CyBench") + WMDP-Cyber + AgentHarm + AgentDojo + MASK + MakeMeSay + Sycophancy

This makes **direct cross-company comparison nearly impossible** — which is exactly the problem this awesome repo aims to solve.

---

## 8. Documentation Maturity

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **First cyber-specific benchmark** | GPT-4o (Aug 2024) | Claude 3 (Mar 2024) | Phuong et al. (Mar 2024) | Grok 4 (Aug 2025) |
| **Total documents w/ cyber benchmarks** | 21 | 24 | 25+ | 9 |
| **System card page count (latest)** | ~50-80p | 213p (Opus 4.6) | ~30-50p | ~20-30p |
| **Open-sources evals?** | No | No | Yes (In-house CTF via Inspect) | No (uses UK AISI Inspect) |
| **Real-world threat intel published?** | No | Yes (GTG-1002 espionage) | Yes (12,000+ incidents via GTI) | No |
| **Specialized cyber model?** | Aardvark (private beta) | — | Sec-Gemini v1 | — |

---

## 9. Timeline

| Date | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| 2023.03 | GPT-4: Low | — | — | — |
| 2023.07 | — | Claude 2: qualitative | — | — |
| 2023.12 | — | — | Gemini 1.0: rudimentary | Grok-1: no eval |
| 2024.03 | — | Claude 3: ASL-2 | Gemini 1.0: early warning (Phuong et al.) | — |
| 2024.06 | — | Claude 3.5 Sonnet: ASL-2 | — | — |
| 2024.08 | GPT-4o: Low | — | — | — |
| 2024.09 | o1-preview/o1-mini: Low | — | — | — |
| 2024.10 | — | Claude 3.5 Haiku/Sonnet (upgraded): ASL-2 | — | — |
| 2024.12 | o1: Low | — | — | — |
| 2025.01 | o3-mini: Low | — | — | — |
| 2025.02 | Deep Research: **Medium** | Claude 3.7 Sonnet: ASL-2 (Cybench 35.9%) | — | — |
| 2025.04 | o3/o4-mini: Below High | — | Gemini 2.5 Pro: CCL alert; Sec-Gemini v1 | — |
| 2025.05 | — | Claude Opus 4: **ASL-3** | Stealth/Situational Awareness paper | — |
| 2025.07 | ChatGPT Agent: refactored CTF | — | Gemini 2.5 Technical Report | — |
| 2025.08 | GPT-5: Below High | Opus 4.1: ASL-3 | Gemini 2.5 Deep Think: CCL alert | Grok 4: below human pro |
| 2025.09 | GPT-5-Codex: Below High | Sonnet 4.5: ASL-3 (Cybench 76.5%) | — | Grok 4 Fast: WMDP-Cyber 81.4% |
| 2025.10 | — | Haiku 4.5: ASL-2 | FSF v3.0 published | — |
| 2025.11 | GPT-5.1-Codex-Max: Below High (~76% CTF) | Opus 4.5: ASL-3 (Cybench 82%) | Gemini 3 Pro: CCL alert, not met | Grok 4.1: WMDP-Cyber 84% |
| 2025.12 | GPT-5.2-Codex: Below High (CVE-Bench 87%) | — | Gemini 3 Flash | — |
| 2026.01 | — | Cyber Ranges Report (Sonnet 4.5) | — | — |
| 2026.02 | GPT-5.3-Codex: **HIGH** (CVE-Bench 90%, Cyber Range 80%) | Opus 4.6: ASL-3 (Cybench 93%); Sonnet 4.6: ASL-2 | Gemini 3.1 Pro: CCL alert, not met | — |

---

## 10. Sources

### OpenAI
- [Preparedness Framework v2](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf)
- [GPT-4 System Card](https://cdn.openai.com/papers/gpt-4-system-card.pdf)
- [GPT-4o System Card](https://cdn.openai.com/gpt-4o-system-card.pdf)
- [o1 System Card (Sep 2024)](https://cdn.openai.com/o1-system-card.pdf)
- [o1 System Card (Dec 2024)](https://cdn.openai.com/o1-system-card-20241205.pdf)
- [Operator System Card](https://cdn.openai.com/operator_system_card.pdf)
- [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf)
- [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf)
- [GPT-4.5 System Card](https://cdn.openai.com/gpt-4-5-system-card-2272025.pdf)
- [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf)
- [Codex Addendum](https://cdn.openai.com/pdf/8df7697b-c1b2-4222-be00-1fd3298f351d/codex_system_card.pdf)
- [ChatGPT Agent System Card](https://cdn.openai.com/pdf/6bcccca6-3b64-43cb-a66e-4647073142d7/chatgpt_agent_system_card_launch.pdf)
- [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf)
- [GPT-5-Codex Addendum](https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf)
- [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf)
- [GPT-5.2 System Card Update](https://cdn.openai.com/pdf/3a4153c8-c748-4b71-8e31-aecbde944f8d/oai_5_2_system-card.pdf)
- [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf)
- [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf)
- [Strengthening Cyber Resilience](https://openai.com/index/strengthening-cyber-resilience/)

### Anthropic
- [RSP v1.0](https://www-cdn.anthropic.com/1adf000c8f675958c2ee23805d91aaade1cd4613/responsible-scaling-policy.pdf)
- [RSP v2.2](https://www.anthropic.com/responsible-scaling-policy)
- [Claude 2 Model Card](https://www.anthropic.com/claude-2-model-card)
- [Claude 3 Model Card](https://www-cdn.anthropic.com/c6a80a657af445f40e31afac050f3bf76d3b1404.pdf)
- [Claude 3.5 Sonnet Addendum](https://www-cdn.anthropic.com/fed9cc193a14b84131812372d8d5857f8f304c52/Model_Card_Claude_3_Addendum.pdf)
- [Claude 3.5 Haiku / Upgraded 3.5 Sonnet Addendum](https://www-cdn.anthropic.com/c7822cdc35ad788ec87e14b3a9d45010f1f86c38.pdf)
- [Claude 3.7 Sonnet System Card](https://anthropic.com/claude-3-7-sonnet-system-card)
- [Claude Opus 4 & Sonnet 4 System Card](https://www.anthropic.com/claude-4-system-card)
- [Claude Opus 4.1 System Card Addendum](https://www.anthropic.com/claude-opus-4-1-system-card)
- [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card)
- [Claude Haiku 4.5 System Card](https://www.anthropic.com/claude-haiku-4-5-system-card)
- [Claude Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card)
- [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card)
- [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card)
- [ASL-3 Deployment Safeguards](https://www.anthropic.com/asl3-deployment-safeguards)
- [Activating ASL-3 Protections](https://www.anthropic.com/activating-asl3-report)
- [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/)
- [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/)
- [Progress from Frontier Red Team](https://www.anthropic.com/news/strategic-warning-for-ai-risk-progress-and-insights-from-our-frontier-red-team)
- [Disrupting AI Espionage](https://www.anthropic.com/news/disrupting-AI-espionage)
- [AI Models on Realistic Cyber Ranges](https://red.anthropic.com/2026/cyber-toolkits-update/)
- [Pilot Sabotage Risk Report](https://alignment.anthropic.com/2025/sabotage-risk-report/)

### Google
- [FSF v1.0](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/introducing-the-frontier-safety-framework/fsf-technical-report.pdf)
- [FSF v3.0](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf)
- [Gemini 1.0 Technical Report](https://arxiv.org/abs/2312.11805)
- [Gemini 1.5 Technical Report](https://arxiv.org/abs/2403.05530)
- [Gemini 2.5 Technical Report](https://arxiv.org/abs/2507.06261)
- [Gemini 2.0 Flash Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf)
- [Gemini 2.5 Pro Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2.5-pro.pdf)
- [Gemini 2.5 Flash Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Flash-Model-Card.pdf)
- [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf)
- [Gemini 3 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-Pro-Model-Card.pdf)
- [Gemini 3 Flash Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-Flash-Model-Card.pdf)
- [Gemini 3.1 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf)
- [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf)
- [Phuong et al. 2024 — Dangerous Capabilities](https://arxiv.org/abs/2403.13793)
- [Evaluating Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- [Defending Gemini Against Prompt Injections](https://arxiv.org/abs/2505.14534)
- [Sec-Gemini v1](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html)
- [Model Cards Index](https://deepmind.google/models/model-cards/)

### xAI
- [Risk Management Framework (Draft)](https://data.x.ai/2025.02.20-RMF-Draft.pdf)
- [Risk Management Framework (Updated)](https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf)
- [Frontier AI Framework (FAIF)](https://data.x.ai/2025-12-31-xai-frontier-artificial-intelligence-framework.pdf)
- [Grok-1 Model Card](https://x.ai/news/grok/model-card)
- [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf)
- [Grok Code Fast 1 Model Card](https://data.x.ai/2025-08-26-grok-code-fast-1-model-card.pdf)
- [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf)
- [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf)
- [xAI Safety](https://x.ai/safety)

### Third-party
- [US/UK AISI Joint Test — o1](https://www.nist.gov/system/files/documents/2024/12/18/US_UK_AI%20Safety%20Institute_%20December_Publication-OpenAIo1.pdf)
- [Framework for Evaluating Emerging Cyberattack Capabilities](https://arxiv.org/abs/2503.11917)
- [Cybench](https://cybench.github.io/) — Stanford University ([arxiv:2408.08926](https://arxiv.org/abs/2408.08926))
- [CyberGym](https://github.com/UC-Berkeley-RDI/cybergym) — UC Berkeley RDI
- [CTI-Bench](https://github.com/xashru/cti-bench) — Rochester IT
- [WMDP](https://www.wmdp.ai/) — Center for AI Safety
- [AgentHarm](https://arxiv.org/abs/2410.09024) — EPFL, Gray Swan, UK AISI, Oxford, CMU
- [MASK](https://arxiv.org/abs/2503.03750) — CAIS
- [MakeMeSay](https://github.com/openai/evals/tree/main/evals/elsuite/make_me_say) — OpenAI / Google DeepMind
