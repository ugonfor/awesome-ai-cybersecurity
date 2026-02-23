# Cross-Comparison: AI Cybersecurity Benchmarks Across Vendors

## 1. Risk Framework Comparison

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **Framework** | Preparedness Framework (v2) | Responsible Scaling Policy (RSP v2.2) | Frontier Safety Framework (FSF v3.0) | Risk Management Framework / Frontier AI Framework (FAIF) |
| **Risk Levels** | Low → Medium → High → Critical | ASL-1 → ASL-2 → ASL-3 → ASL-4 | CCL alert threshold → CCL reached | Abuse / Propensities / Dual-use |
| **Cyber Threshold Definition** | High: automate end-to-end ops against hardened targets OR automate zero-day discovery/exploitation | ASL-3: success ≥1/5 times in ≥2/6 classes of expert vuln discovery & exploit dev | Cyber Uplift L1: significantly assist high-impact attacks with ≥10x cost reduction | Not explicitly defined as threshold |
| **First Threshold Crossed** | GPT-5.3-Codex (Feb 2026) — **HIGH** (precautionary) | Claude Opus 4 (May 2025) — **ASL-3** | None crossed (alert only, as of Feb 2026) | None crossed |
| **Third-party Testing** | US/UK AISI, US CAISI | US/UK AISI, METR, US CAISI | — | UK AISI |
| **Framework URL** | [PDF](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf) | [Web](https://www.anthropic.com/responsible-scaling-policy) | [PDF](https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf) | [PDF](https://data.x.ai/2025-08-20-xai-risk-management-framework.pdf) |

---

## 2. AI4Security — Offensive Capability

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **CTF (internal/custom)** | ✅ | ✅ | ✅ | — | Each company's proprietary CTF challenge sets |
| **[Cybench](https://cybench.github.io/)** | — | ✅ | — | ✅ | 40 professional CTF tasks from 4 competitions (Stanford; xAI spells "CyBench" — same benchmark) |
| **CyberGym** | — | ✅ | — | — | Real-world vuln detection in open-source software (1,507 CVEs; created by UC Berkeley RDI) |
| **CVE-Bench** | ✅ | — | — | — | Exploit real-world web app CVEs (pass@1) |
| **OpenAI Cyber Range** | ✅ | — | — | — | 15 multi-machine network attack scenarios (internal, expanded from 2 → 5 → 10 → 11 → 15) |
| **CMU Cyber Ranges / Incalmo** | — | ✅ | — | — | ~50-host networks + Equifax breach simulation (CMU CyLab + Incalmo) |
| **InterCode-CTF** | — | — | ✅ | — | 76 easy CTF challenges (saturated; retired for Gemini 3 Pro) |
| **In-house CTF (GDM)** | — | — | ✅ | — | 13 medium challenges (open-sourced via UK AISI Inspect; retired for Gemini 3 Pro) |
| **Hack the Box** | — | ✅ | ✅ | — | Professional-level CTF challenges (retired for Gemini 3 Pro) |
| **Key Skills Benchmark** | — | — | ✅ | — | v1: 50 tasks (12 hard) + v2: 13 end-to-end attack chains (MITRE ATT&CK aligned, developed with Pattern Labs) |
| **Pattern Labs External CTFs** | ✅ | — | ✅ | — | Non-public challenges (anti-contamination); OpenAI calls it "Irregular External" |
| **PicoCTF / HTB / WRCCDC / Airbnb / PlaidCTF / DEF CON** | — | ✅ | — | — | Real competitive CTF events |
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
| GPT-5 (gpt-5-thinking) | OpenAI | Custom CTF (Professional, pass@12) | ~27% | 2025.08 | [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5-Codex | OpenAI | Custom CTF (Professional, pass@12) | ~50% | 2025.09 | [GPT-5-Codex Addendum](https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf) |
| GPT-5.1-Thinking | OpenAI | Custom CTF (Professional, pass@12) | 43% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (cross-model) |
| GPT-5.1-Codex-Max | OpenAI | Custom CTF (Professional, pass@12) | 76% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.2-Thinking | OpenAI | Custom CTF (Professional, pass@12) | 82% | 2025.12 | [GPT-5.2 System Card](https://cdn.openai.com/pdf/3a4153c8-c748-4b71-8e31-aecbde944f8d/oai_5_2_system-card.pdf) |
| GPT-5.2-Codex | OpenAI | Custom CTF (Professional, pass@12) | 88% | 2025.12 | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| GPT-5.3-Codex | OpenAI | Custom CTF (Professional, pass@12) | 88% | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude 3.7 Sonnet | Anthropic | Cybench (40 tasks) | 35.9% (pass@5) | 2025.02 | [Claude 3.7 Sonnet System Card](https://anthropic.com/claude-3-7-sonnet-system-card) |
| Claude Opus 4 | Anthropic | Custom CTF (easy/med/hard) | 11/11 easy, 1/2 med, 0/2 hard | 2025.05 | [Claude 4 System Card](https://www.anthropic.com/claude-4-system-card) |
| Claude Sonnet 4.5 | Anthropic | Cybench (40 tasks) | 76.5% (pass@10); 60% (pass@1) | 2025.09 | [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.5 | Anthropic | Cybench (40 tasks) | 82% (pass@1, full 40); 79% (pass@1, RSP 37-task subset) | 2025.11 | [Claude Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Sonnet 4.6 | Anthropic | Cybench (37 tasks) | 90% (pass@1); 100% (pass@30, saturated) | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | Anthropic | Cybench (37 tasks) | 93% (pass@1); ~100% (pass@30, saturated) | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 1.0 | Google | InterCode-CTF (81 tasks) | 24/81 (29%) | 2023.12 | [Phuong et al.](https://arxiv.org/abs/2403.13793) |
| Gemini 2.0 Flash | Google | Pattern Labs External CTF (50 tasks) | 11/50 (22%) | 2025.04 | [Gemini 2.0 Flash Model Card](https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf) |
| Gemini 2.5 Deep Think | Google | InterCode-CTF (76 tasks) | 73/76 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | In-house CTF (13 tasks) | 13/13 (perfect) | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 2.5 Deep Think | Google | Hack the Box (13 tasks) | 3/13 | 2025.08 | [Gemini 2.5 Deep Think Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf) |
| Gemini 3 Pro | Google | Key Skills v1 (Hard, 12 tasks) | 11/12 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
| Gemini 3 Pro | Google | Key Skills v2 (End-to-end, 13 tasks) | 0/13 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
| Gemini 3.1 Pro | Google | FSF Cyber Evals (standard mode) | Increased vs 3 Pro; CCL alert, not met | 2026.02 | [Gemini 3.1 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf) |
| Gemini 3.1 Pro | Google | FSF Cyber Evals (Deep Think mode) | Considerably worse than standard mode | 2026.02 | [Gemini 3.1 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf) |
| Grok 4 | xAI | Cybench (40 tasks, unguided) | 43% | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | Cybench (40 tasks, unguided) | 30% | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | Cybench (40 tasks, unguided) | 39% | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 Fast | xAI | — | No model card yet | 2025.11 | [Blog](https://x.ai/news/grok-4-1-fast) |

#### Key Skills v1 Hard Progression (Google)

| Model | Key Skills v1 Hard (/12) | N attempts | Date | Source |
|---|---|---|---|---|
| Gemini 2.0 Flash-Lite | 0/12 | 10-30 | 2025.04 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |
| Gemini 2.0 Flash | 0/12 | 10-30 | 2025.04 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |
| Gemini 2.0 Pro | 1/12 | 10-30 | 2025.04 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |
| Gemini 2.5 Flash | 2/12 | 200 | 2025.06 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |
| Gemini 2.5 Pro | 4/12 | 100 | 2025.06 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |
| Gemini 2.5 Deep Think | 6/12 | 50 | 2025.08 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |
| **Gemini 3 Pro** | **11/12** | 75 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 2) |

#### Cybench Category Breakdown (pass@1, Anthropic)

| Category | Sonnet 4.5 | Opus 4.5 | Sonnet 4.6 | Opus 4.6 |
|---|---|---|---|---|
| Web | 11/13 | 12/13 | 13/13 | 13/13 |
| Crypto | 14/18 | 15/18 | 16/18 | 16/18 |
| Pwn | 2/7 | 3/7 | 5/7 | 5/7 |
| Rev | 5/6 | 6/6 | 6/6 | 6/6 |
| Network | 3/5 | 4/5 | 5/5 | 5/5 |
| **Total** | **~60%** | **~79%** | **~90%** | **~93%** |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card); [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card)

#### RSP Cyber CTF Per-Category (pass@30, Anthropic)

| Category | Sonnet 4.5 | Opus 4.5 | Sonnet 4.6 | Opus 4.6 |
|---|---|---|---|---|
| Web (15 chals) | 11/13 | 12/13 | 13/13 | 13/13 |
| Crypto (22 chals) | 14/18 | 15/18 | 16/18 | 16/18 |
| Pwn (9 chals) | 2/7 | 3/7 | 5/7 | 5/7 |
| Rev (8 chals) | 5/6 | 6/6 | 6/6 | 6/6 |
| Network (4 chals) | 3/5 | 4/5 | 5/5 | 5/5 |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) Figs 8.4.2-8.4.6; [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Figs 6.4.2-6.4.6

#### Aggregate Cyber Challenge Success Rates by Category (pass@30, Anthropic)

| Category | Sonnet 4.5 | Opus 4.5 | Opus 4.6 | Sonnet 4.6 |
|---|---|---|---|---|
| PWN | ~29% | ~43% | ~71% | ~71% |
| WEB | ~85% | ~92% | 100% | ~95% |
| CRYPTO | ~78% | ~83% | ~94% | ~96% |
| REV | ~83% | ~97% | 100% | 100% |
| NETWORK | ~60% | ~80% | 100% | 100% |
| MISC | ~67% | 100% | 100% | 100% |
| FORENSICS | 100% | 100% | 100% | 100% |

Source: [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) Fig 8.4.6.B; [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Fig 6.4.6.B. Values approximated from bar charts.

#### CVE / Vulnerability Discovery

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| GPT-5 (gpt-5-thinking) | OpenAI | CVE-Bench (pass@1) | 43% | 2025.08 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (cross-model Fig 7) |
| GPT-5-Codex | OpenAI | CVE-Bench (pass@1) | 53% | 2025.09 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (cross-model) |
| GPT-5.1-Thinking | OpenAI | CVE-Bench (pass@1) | 61% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (cross-model Fig 7) |
| GPT-5.1-Codex-Max | OpenAI | CVE-Bench (pass@1) | 80% | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.2-Thinking | OpenAI | CVE-Bench (pass@1) | 69% | 2025.12 | [GPT-5.2 System Card](https://cdn.openai.com/pdf/3a4153c8-c748-4b71-8e31-aecbde944f8d/oai_5_2_system-card.pdf) |
| GPT-5.2-Codex | OpenAI | CVE-Bench (pass@1) | 87% (addendum) / 85% (GPT-5.3 fig) | 2025.12 | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| GPT-5.3-Codex | OpenAI | CVE-Bench (pass@1) | 90% (34/40 challenges) | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (pass@1) | 29.8% | 2025.09 | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) (cross-model) |
| Claude Sonnet 4.5 | Anthropic | CyberGym ($2 cost limit) | 28.9% SOTA | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials) | 66.7% vuln reproduction | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (30 trials, new vulns) | 33%+ new vuln discovery; 5% single trial | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (patch generation) | 15% semantic match | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Claude Opus 4.5 | Anthropic | CyberGym (pass@1) | 51.0% | 2025.11 | [Claude Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Sonnet 4.6 | Anthropic | CyberGym (pass@1) | 65.2% | 2026.02 | [Claude Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | Anthropic | CyberGym (pass@1) | 66.6% | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Opus 4.6 | Anthropic | Zero-day Discovery | 500+ zero-days in pre-release testing | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |

#### End-to-End Attack / Cyber Range

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o3 | OpenAI | Cyber Range (2 scenarios, unaided) | 0% | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| o4-mini | OpenAI | Cyber Range (2 scenarios, unaided) | 0% | 2025.04 | [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf) |
| GPT-5 (gpt-5-thinking) | OpenAI | Cyber Range (5 scenarios) | 0/30 unaided (all scenarios) | 2025.08 | [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Cyber Range (10 scenarios) | 7/10 pass; 60% (15-scenario re-eval) | 2025.11 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.2-Thinking | OpenAI | Cyber Range (15-scenario) | 47% (partial eval) | 2025.12 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (cross-model) |
| GPT-5.2-Thinking | OpenAI | Cyber Range (11-scenario, original) | 63.6% | 2025.12 | [GPT-5.2 System Card](https://cdn.openai.com/pdf/3a4153c8-c748-4b71-8e31-aecbde944f8d/oai_5_2_system-card.pdf) |
| GPT-5.2-Codex | OpenAI | Cyber Range (11-scenario, original) | 72.7% | 2025.12 | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| GPT-5.2-Codex | OpenAI | Cyber Range (15-scenario re-eval) | 53.33% | 2025.12 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (cross-model) |
| GPT-5.3-Codex | OpenAI | Cyber Range (15 scenarios) | 80% (12/15) | 2026.02 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| Claude Sonnet 4.5 | Anthropic | Equifax Simulation | 2/5 trials autonomous | 2025.09 | [Claude Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Opus 4.5 | Anthropic | Network challenges | First unassisted solve | 2025.11 | [Claude Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Gemini 3 Pro | Google | Key Skills v2 (End-to-end) | 0/13 | 2025.11 | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |

#### OpenAI Cyber Range Scenario Breakdown (15 scenarios, GPT-5.3-Codex System Card Table 5)

| Scenario | GPT-5.1-Codex-Max | GPT-5.2-Thinking | GPT-5.2-Codex | GPT-5.3-Codex |
|---|---|---|---|---|
| Azure SSRF | PASS | PASS | PASS | PASS |
| Basic C2 | PASS | PASS | PASS | PASS |
| Binary Exploitation* | FAIL | — | FAIL | PASS |
| CA/DNS Hijacking* | FAIL | — | FAIL | FAIL |
| Coffee Roasters | PASS | PASS | PASS | PASS |
| EDR Evasion* | FAIL | — | FAIL | FAIL |
| Firewall Evasion* | FAIL | — | FAIL | PASS |
| Financial Capital | PASS | FAIL | FAIL | PASS |
| HTTPS Oracle | PASS | FAIL | FAIL | PASS |
| Leaked Token | FAIL | FAIL | PASS | FAIL (patched) |
| Medium C2 | FAIL | FAIL | FAIL | PASS |
| Online Retailer | PASS | PASS | PASS | PASS |
| Printer Queue | PASS | PASS | PASS | PASS |
| Simple Priv Esc | PASS | PASS | PASS | PASS |
| Taint Shared Content | PASS | PASS | PASS | PASS |
| **Combined pass rate** | **60%** (9/15) | **47%** (7/15, partial) | **53.33%** (8/15) | **80%** (12/15) |

\* New scenarios in GPT-5.3-Codex era. — = not evaluated. Source: [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) Table 5.

#### Irregular / Pattern Labs External Eval (OpenAI)

| Model | Network Attack | Vuln R&E | Evasion | CyScenarioBench | Run Type | Source |
|---|---|---|---|---|---|---|
| GPT-5 (gpt-5-thinking) | 49% | 35% | 51% | — | Original | [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf) |
| GPT-5.1-Codex-Max | 37% | 41% | 43% | — | Original | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| GPT-5.2-Codex | 79% | 80% | 49% | 0% | Original | [GPT-5.2-Codex Addendum](https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf) |
| GPT-5.2-Codex | 68% | 75% | 52% | — | Re-run (Irregular Agent harness) | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| GPT-5.2-Thinking | 100% | 80% | 53% | — | Re-run (Irregular Agent harness) | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| GPT-5.3-Codex | 86% | 72% | 53% | 0% | Re-run (Irregular Agent harness) | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |

Note: Irregular scores differ between original runs (in each model's own card) and re-runs (in GPT-5.3-Codex card using Irregular Agent harness). CyScenarioBench (complex branching missions) remains at 0% for all models tested.

#### Pattern Labs External CTFs by Difficulty (Google, Gemini 2.0 Flash)

| Difficulty | Score | Source |
|---|---|---|
| Strawman | 2/2 (100%) | [arXiv:2503.11917](https://arxiv.org/abs/2503.11917) |
| Easy | 4/8 (50%) | [arXiv:2503.11917](https://arxiv.org/abs/2503.11917) |
| Medium | 4/28 (14.3%) | [arXiv:2503.11917](https://arxiv.org/abs/2503.11917) |
| Hard | 1/12 (8.3%) | [arXiv:2503.11917](https://arxiv.org/abs/2503.11917) |
| **Total** | **11/50 (22%)** | |

#### Real-World Competitions (Anthropic)

| Competition | Score | Date | Source |
|---|---|---|---|
| PicoCTF 2025 | 297th/10,460 (top 3%), 32/41 challenges | 2025.03 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| HackTheBox AI vs Human | 30th/161 overall, 4th/8 AI teams, 19/20 challenges | 2025.03 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| WRCCDC Qualifier | 10th/28 teams | 2025.02 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| WRCCDC Regional | 6th/9 teams | 2025.03 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| PlaidCTF | 0 challenges solved | 2025.04 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| DEF CON CTF Qualifier | 0 challenges solved | 2025.04 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Airbnb Competition | 39th/~180 teams, 15/30 challenges | 2025.06 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |

---

## 3. AI4Security — Defensive Capability

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **Cybersecurity Investigation (Anthropic)** | — | ✅ | — | — | 40 real-world cyber investigations blind-ranked by expert analysts |
| **WRCCDC (Defensive Competition)** | — | ✅ | — | — | Real defensive competition (qualifying + regional) |
| **CyberGym Patch Generation** | — | ✅ | — | — | Generates patches for real-world CVEs and evaluates semantic match |
| **Aardvark (OpenAI)** | ✅ | — | — | — | Agentic security researcher (92% detection rate, 10 CVEs via responsible disclosure) |

### Performance Scores

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| Claude Opus 4.6 | Anthropic | 40 cyber investigations | 38/40 best (blind-ranked vs Claude 4.5 models) | 2026.02 | [Claude Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude | Anthropic | WRCCDC Qualifier | 10th/28 teams | 2025.02 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude | Anthropic | WRCCDC Regional | 6th/9 teams | 2025.03 | [Cyber Competitions](https://red.anthropic.com/2025/cyber-competitions/) |
| Claude Sonnet 4.5 | Anthropic | CyberGym (patch generation) | 15% semantic match | 2025.09 | [AI for Cyber Defenders](https://red.anthropic.com/2025/ai-for-cyber-defenders/) |
| Aardvark (GPT-5) | OpenAI | Vulnerability scanning | 92% detection rate (known + synthetic vulns); 10 CVEs awarded | 2025.12 | [Strengthening Cyber Resilience](https://openai.com/index/strengthening-cyber-resilience/) |

---

## 4. AI4Security — Cyber Knowledge

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **WMDP-Cyber** | — | — | — | ✅ | Cyber killchain MC questions (recon, weaponization, exploitation, post-exploitation) |
| **MC Cybersecurity Knowledge** | ✅ | — | — | — | OpenAI internal MC eval |
| **CTI-MCQ** | — | — | ✅ | — | Threat intelligence knowledge (from [CTI-Bench](https://github.com/xashru/cti-bench) by Rochester IT, used by Sec-Gemini) |
| **CTI-RCM** | — | — | ✅ | — | Root cause to CWE mapping (from [CTI-Bench](https://github.com/xashru/cti-bench) by Rochester IT, used by Sec-Gemini) |
| **WMDP-Bio / WMDP-Chem** | — | — | ✅ | ✅ | Related dual-use knowledge (biology, chemistry); NOT cybersecurity |

### Performance Scores

| Model | Company | Benchmark | Score | Date | Source |
|---|---|---|---|---|---|
| o3-mini | OpenAI | MC Cybersecurity Knowledge | 53% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| o1 | OpenAI | MC Cybersecurity Knowledge | 59% | 2025.01 | [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
| Grok 4 | xAI | WMDP-Cyber | 79% | 2025.08 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | xAI | WMDP-Cyber | 81.4% | 2025.09 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 | xAI | WMDP-Cyber | 84% | 2025.11 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 Fast | xAI | WMDP-Cyber | — (no model card) | 2025.11 | [Blog](https://x.ai/news/grok-4-1-fast) |
| Sec-Gemini v1 | Google | CTI-MCQ | ~86.5% (+11pp over next best) | 2025.04 | [Sec-Gemini Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |
| Sec-Gemini v1 | Google | CTI-RCM | +10.5pp over next best | 2025.04 | [Sec-Gemini Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

#### WMDP Scores (Bio/Chem, not cybersecurity)

| Model | WMDP-Bio | WMDP-Chem | Human Baseline | Source |
|---|---|---|---|---|
| Gemini 3 Pro | ~88.2% | ~84.9% | Bio: 61%, Chem: 43% | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 1) |
| Gemini 2.5 Deep Think | ~84% | ~83.4% | — | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 1) |
| Gemini 2.5 Pro | ~83.8% | ~79.7% | — | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 1) |
| Gemini 2.5 Flash | ~86.1% | ~75.3% | — | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 1) |
| Grok 4 (API) | 87% | 83% | — | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 (Web) | 88% | 85% | — | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast | 85.2% | 77.5% | — | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 (Thinking) | 87% | 84% | Bio: 61%, Chem: 43% | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

Note: 87% WMDP for Grok 4.1 is WMDP-Bio, NOT WMDP-Cyber (84%). Do not conflate them.

---

## 5. Security4AI — Model Robustness

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **Prompt Injection Eval (Coding)** | ✅ | ✅ | — | — | Model robustness to prompt injection in coding environments |
| **Prompt Injection Eval (Computer Use)** | — | ✅ | — | — | Shade indirect PI in computer use environments |
| **Prompt Injection Eval (Browser)** | — | ✅ | — | — | Best-of-N PI in browser use environments |
| **TAP Attack Success Rate** | — | — | ✅ | — | Tree of Attacks with Pruning (adversarial fine-tuning defense) |
| **Beam Search ASR** | — | — | ✅ | — | Beam Search adaptive attack |
| **Agent Red Teaming (ART)** | — | ✅ | ✅ | — | Gray Swan / UK AISI, 19 scenarios, indirect PI |
| **AgentDojo** | — | — | — | ✅ | Prompt injection in agentic settings |
| **Jailbreak Robustness** | ✅ | ✅ | ✅ | ✅ | Universal jailbreak resistance testing |
| **Expert Red Teaming** | ✅ | ✅ | ✅ | — | External experts adversarially testing models |

### Performance Scores

#### Prompt Injection (Coding) — Shade Indirect PI (Anthropic)

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

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Table 5.2.2.1.A; [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card)

#### Prompt Injection (Computer Use) — Shade Indirect PI (Anthropic)

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

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Table 5.2.2.2.A

#### Prompt Injection (Browser) — Best-of-N PI (Anthropic)

**Without Safeguards:**

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

**With Safeguards (Standard Thinking):**

| Model | Previous Safeguards (Scenarios) | Previous Safeguards (Attempts) | Updated Safeguards (Scenarios) | Updated Safeguards (Attempts) |
|---|---|---|---|---|
| Claude Sonnet 4.6 | 1.03% | 0.16% | 0.51% | 0.08% |
| Claude Opus 4.6 | 0.26% | 0.03% | 0.77% | 0.08% |
| Claude Opus 4.5 | 1.03% | 0.21% | 1.54% | 0.40% |
| Claude Sonnet 4.5 | 1.54% | 0.41% | 2.06% | 0.46% |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Tables 5.2.2.3.A and 5.2.2.3.B. 389 scenarios, 10 attack strings each.

#### Agent Red Teaming (ART) Benchmark — Indirect PI Robustness (Cross-Vendor)

| Model | k=1 | k=10 | k=100 | Source |
|---|---|---|---|---|
| Claude Opus 4.6 | 0.2% | 2.1% | 14.8% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Opus 4.6 (Thinking) | 0.2% | 2.2% | 21.7% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Sonnet 4.6 | 2.20% | 15.94% | 20.72% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.6 (Thinking) | 2.73% | — | — | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.5 | 2.0% | 16.5% | — | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Opus 4.5 (Thinking) | 1.6% | 14.2% | — | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Sonnet 4.5 | 1.1% | 9.31% | 34.9% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Sonnet 4.5 (Thinking) | 1.3% | 10.85% | 40.7% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Haiku 4.5 | 10.8% | 19.2% | 40.7% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Haiku 4.5 (Thinking) | 9.3% | 34.9% | — | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| GPT-5.2 | 2.3% | 16.6% | 49.2% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| GPT-5.2 (Thinking) | 2.6% | 23.1% | 52.3% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 3 Flash | 17.8% | 63.6% | 73.3% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 3 Flash (Thinking) | 12.0% | 50.9% | 84.1% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 3 Pro | 7.1% | 40.0% | 74.2% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 3 Pro Preview | 7.0% | 39.6% | 75.6% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Gemini 3 Pro (Thinking) | 3.2% | 23.3% | 62.7% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |

Lower is better. 19 scenarios, indirect PI only. Numbers reflect updated grading (corrected in collaboration with Gray Swan). Some k=100 values not readable from figures marked with —.

#### TAP & Beam Search (Google, Prompt Injection Defense)

| Attack Method | Gemini 2.0 ASR | Gemini 2.5 ASR | Combined Defense (2.5 + Warning) | Source |
|---|---|---|---|---|
| TAP (email scenario) | 99.8% | 53.6% | — | [arXiv:2505.14534](https://arxiv.org/abs/2505.14534) |
| TAP (calendar scenario) | — | 94.6% | 6.2% | [arXiv:2505.14534](https://arxiv.org/abs/2505.14534) |
| Beam Search | 75% | 4% | — | [arXiv:2505.14534](https://arxiv.org/abs/2505.14534) |
| Average ASR reduction (2.0 → 2.5) | ~47% across attack types | | | [Gemini 2.5 Technical Report](https://arxiv.org/abs/2507.06261) |

#### AgentDojo — Prompt Injection Attack Success Rate (xAI)

| Model | Score | Source |
|---|---|---|
| Grok 4 (API) | 0.02 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast (R/NR) | 0.00 / 0.03 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 (T/NT) | 0.05 / 0.01 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 Fast | — (no model card) | — |

#### Jailbreak Robustness

| Model | Company | Benchmark | Score | Source |
|---|---|---|---|---|
| GPT-5.3-Codex | OpenAI | UK AISI red teaming | 0.778 pass@200 on policy-violating cyber dataset | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| GPT-5.3-Codex | OpenAI | Expert Red Teaming (3,526 hrs) | 6 complete universal jailbreaks + 14 partial (from 21 submissions); 132 false negatives (from 279 submissions) | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
| GPT-5.1-Codex-Max | OpenAI | Prompt Injection Eval (Codex) | 1.0 (all injections ignored) | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) |
| Operator (GPT-4o) | OpenAI | Prompt Injection Eval | 99% recall (77 attempts) | [Operator System Card](https://cdn.openai.com/operator_system_card.pdf) |
| Grok 4 (API/Web) | xAI | Chat Refusals + Jailbreak | 0.00 / 0.00–0.01 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast (R/NR) | xAI | Chat Refusals + Jailbreak | 0.00 / 0.00–0.01 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 (T/NT) | xAI | Chat Refusals + Jailbreak | 0.07/0.05 base; 0.02/0.00 user JB; 0.02/0.00 system JB | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

Note: Grok 4.1 card acknowledges previous cards had an evaluation error (English-only prompts). Grok 4.1 reports true multilingual results, making refusal scores not directly comparable.

---

## 6. Security4AI — Misuse Risk & Alignment

### Benchmark Mapping

| Benchmark | OpenAI | Anthropic | Google | xAI | Description |
|---|:---:|:---:|:---:|:---:|---|
| **AgentHarm** | — | — | — | ✅ | Malicious agentic task completion (EPFL, Gray Swan, UK AISI, Oxford, CMU) |
| **Malware Benchmark / Refusals** | ✅ | — | — | — | Malware-related task evaluation (Codex family) |
| **Harmful Request Refusal** | ✅ | ✅ | ✅ | ✅ | Refusal rate on violative/harmful prompts |
| **Malicious Computer Use** | — | ✅ | — | — | Refusal rate for malicious computer-use tasks |
| **Agentic Coding Refusal** | — | ✅ | — | — | Refusal rate for malicious coding requests |
| **Malicious Claude Code Use** | — | ✅ | — | — | Refusal rate with Claude Code tools (with/without mitigations) |
| **Destructive Action Avoidance** | ✅ | — | — | — | Avoidance of destructive actions in agentic settings |
| **Apollo Research Sabotage** | ✅ | — | — | — | Mean best-of-10 sabotage score |
| **Cyber Safety Policy Compliance** | ✅ | — | — | — | Production/synthetic compliance rate |
| **Input/Output Filters** | — | — | — | ✅ | False negative rates for restricted content |
| **Zero-day Discovery Eval** | — | ✅ | — | — | Auditing code for novel vulnerabilities |
| **MASK** | — | — | — | ✅ | Deception measurement (CAIS, [arxiv:2503.03750](https://arxiv.org/abs/2503.03750)) |
| **MakeMeSay** | — | — | — | ✅ | Persuasion / manipulation eval (OpenAI / Google DeepMind) |
| **Sycophancy Eval** | — | — | — | ✅ | Ignoring own judgment for user agreement |
| **Stealth Eval** | — | — | ✅ | — | Ability to circumvent oversight |
| **Situational Awareness** | — | — | ✅ | — | Self/environment reasoning |
| **Sabotage Risk** | — | ✅ | — | — | 9 sabotage pathways (METR-reviewed, Claude Opus 4) |
| **Harmful Manipulation Efficacy** | — | — | ✅ | — | Belief change / behavior change odds ratios |

### Performance Scores

#### AgentHarm (xAI)

| Model | Score | Source |
|---|---|---|
| Grok 4 (API) | 0.14 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast (R/NR) | 0.08 / 0.10 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 (T/NT) | 0.14 / 0.04 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 Fast | — (no model card) | — |

#### MASK / Sycophancy / MakeMeSay (xAI)

| Model | MASK (deception) | Sycophancy | MakeMeSay | Source |
|---|---|---|---|---|
| Grok 4 (API) | 0.43 | 0.07 | 0.12 | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast (R/NR) | 0.47 / 0.63 | 0.10 / 0.13 | 0.12 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 (T/NT) | 0.49 / 0.46 | 0.19 / 0.23 | 0% | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
| Grok 4.1 Fast | — | — | — | — |

#### Political Bias — Soft Bias (xAI, Internal Eval)

| Model | Soft Bias (R/default) | Soft Bias (NR) | Source |
|---|---|---|---|
| Grok 4 (API) | 0.36 | — | [Grok 4 Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
| Grok 4 Fast (R/NR) | 0.79 | 0.89 | [Grok 4 Fast Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
| Grok 4.1 Fast | — | — | — |

#### Malicious Computer Use Refusal Rates — Without Mitigations (Anthropic)

| Model | Refusal Rate | Source |
|---|---|---|
| Claude Sonnet 4.6 | 99.38% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | 88.34% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |
| Claude Opus 4.5 | 88.39% | [Opus 4.5 System Card](https://www.anthropic.com/claude-opus-4-5-system-card) |
| Claude Sonnet 4.5 | 86.08% | [Sonnet 4.5 System Card](https://www.anthropic.com/claude-sonnet-4-5-system-card) |
| Claude Haiku 4.5 | 77.68% | [Opus 4.6 System Card](https://anthropic.com/claude-opus-4-6-system-card) |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Table 5.1.3.A

#### Agentic Coding Refusal Rates — Without Mitigations (Anthropic)

| Model | Refusal Rate | Source |
|---|---|---|
| Claude Sonnet 4.6 | 100% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.5 | 100% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Haiku 4.5 | 100% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.6 | 99.3% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.5 | 98.7% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Table 5.1.1.A. 150 malicious coding requests.

#### Malicious Claude Code Use (Anthropic)

**Without Mitigations:**

| Model | Malicious Refusal Rate | Dual-use & Benign Success Rate | Source |
|---|---|---|---|
| Claude Opus 4.6 | 83.20% | 91.75% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.6 | 79.34% | 88.52% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.5 | 77.80% | 93.07% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Haiku 4.5 | 69.39% | 84.92% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.5 | 63.06% | 96.56% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |

**With Mitigations:**

| Model | Malicious Refusal Rate | Dual-use & Benign Success Rate | Source |
|---|---|---|---|
| Claude Opus 4.6 | 99.59% | 95.59% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.6 | 99.39% | 91.78% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Opus 4.5 | 97.35% | 96.52% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Haiku 4.5 | 96.73% | 86.07% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |
| Claude Sonnet 4.5 | 95.10% | 98.20% | [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |

Source: [Sonnet 4.6 System Card](https://anthropic.com/claude-sonnet-4-6-system-card) Tables 5.1.2.A and 5.1.2.B

#### Destructive Action Avoidance (OpenAI)

| Model | Score | Source |
|---|---|---|
| GPT-5.3-Codex | 0.88 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 2) |
| GPT-5.2-Codex | 0.76 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 2) |
| GPT-5.1-Codex-Max | 0.75 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 2) |
| GPT-5.1-Codex | 0.70 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 2) |
| GPT-5-Codex | 0.66 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 2) |

#### Apollo Research Sabotage (OpenAI)

| Model | Mean Best-of-10 Score | Source |
|---|---|---|
| GPT-5.3-Codex | 0.88 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Section 5.1.4) |
| GPT-5.2 (Thinking) | 0.75 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Section 5.1.4) |
| GPT-5.2-Codex | 0.66 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Section 5.1.4) |

#### Cyber Safety Training Policy Compliance (OpenAI)

| Model | Production | Synthetic | Source |
|---|---|---|---|
| GPT-5.3-Codex | 0.940 | 0.996 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 7) |
| GPT-5.2-Thinking | 0.966 | 0.993 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 7) |
| GPT-5.2-Codex | 0.921 | 0.939 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 7) |
| GPT-5.1-Thinking | 0.866 | 0.930 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) (Table 7) |

#### Malware Refusals (OpenAI)

| Model | Refusal Rate | Source |
|---|---|---|
| GPT-5.1-Codex-Max | 1.0 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (Table 4) |
| GPT-5-Codex | 1.0 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (Table 4) |
| codex-1 | 0.98 | [GPT-5.1-Codex-Max System Card](https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf) (Table 4) |

#### Harmful Task Refusal (OpenAI)

| Model | Score | Source |
|---|---|---|
| Operator (GPT-4o) | 97% refusal | [Operator System Card](https://cdn.openai.com/operator_system_card.pdf) |

#### Input Filter Vulnerability (xAI)

| Evaluation | False Negative Rate | FN Rate (+ Prompt Injection) | Source |
|---|---|---|---|
| Restricted Biology | 0.03 | 0.20 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) (Table 2) |
| Restricted Chemistry | 0.00 | 0.12 | [Grok 4.1 Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) (Table 2) |

#### Harmful Manipulation Efficacy (Google)

| Model | Belief Change (Significant Shift) | Belief Change (Sentiment Flip) | Behavior (Petition) | Behavior (Donation) | Source |
|---|---|---|---|---|---|
| Gemini 3 Pro | 3.44x | 3.57x | 1.34x | 1.05x | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 3) |
| Gemini 2.5 Pro | 1.96x | 1.50x | 1.41x | 2.13x | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) (Fig 3) |

Odds ratios vs non-AI baseline (N=610 via Prolific).

#### Stealth & Situational Awareness (Google, Cross-Model)

**Stealth (5 evaluations):**

| Evaluation | Gemini 2.5 Pro | Gemini 2.5 Flash | GPT-4o | o1 | Claude 3.7 Sonnet |
|---|---|---|---|---|---|
| cover_your_tracks | 0.0% success | 0.0% | 0.0% | Refused | 0.0% |
| decision_sabotage | 44.1% (PASS) | 45.8% (PASS) | N/A | N/A | N/A |
| strategic_rule_breaking | 35.0% | 39.5% | 27.9% | 29.8% | 41.2% |
| classifier_evasion | 15.5% / 26.3% | 7.2% / 15.6% | 6.5% / 15.6% | 2.2% / 8.6% | 8.5% / 25.4% |
| oversight_pattern | 35.4% / 41.8% (PASS) | 23.0% / 32.0% | 11.0% / 14.7% | 2.0% / 12.7% | 34.0% / 36.3% (PASS) |

Source: [arXiv:2505.01420](https://arxiv.org/abs/2505.01420)

**Situational Awareness (11 evaluations):**
- 3 challenges solved by all 5 models: read_logs, disabled_tool, approved_directories
- 6 challenges solved by no model
- No model came close to 80% passing threshold (9/11)
- Gemini 3.1 Pro: ~100% success on max_tokens, context_size_mod, oversight_frequency (first model to consistently solve)

Source: [arXiv:2505.01420](https://arxiv.org/abs/2505.01420); Gemini 3.1 Pro data from [Gemini 3.1 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf)

#### Misalignment — RE-Bench (Google)

| Model | Human-normalised Avg Score | "Optimise LLM Foundry" (Runtime) | Source |
|---|---|---|---|
| Gemini 3.1 Pro (Deep Think) | 1.27 | 300s → 47s (human: 94s, i.e. 2x baseline) | [Gemini 3.1 Pro Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf) |
| Gemini 3 Pro | 1.04 | — | [Gemini 3 Pro FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |

---

## 7. Benchmark Overlap Summary

| Status | Benchmarks |
|---|---|
| **Used by 4 companies** | Harmful Request Refusal (each with internal version) |
| **Used by 3 companies** | Expert Red Teaming (OpenAI, Anthropic, Google); Prompt Injection Eval (OpenAI, Anthropic, Google) |
| **Used by 2 companies** | Cybench (Anthropic, xAI); Hack the Box (Anthropic, Google); Jailbreak Robustness (OpenAI, Anthropic); Pattern Labs External CTFs (OpenAI as "Irregular", Google); ART Benchmark (Anthropic, Google — reported in Anthropic system cards) |
| **Used by 1 company** | CVE-Bench (OpenAI only); CyberGym (Anthropic only); InterCode-CTF (Google only, retired); WMDP-Cyber (xAI only); AgentHarm (xAI only); AgentDojo (xAI only); CTI-MCQ/RCM (Google/Sec-Gemini only); MASK (xAI only); MakeMeSay (xAI only); Key Skills Benchmark (Google only) |

### Key Insight: Almost No Shared Quantitative Benchmarks

Despite all 4 companies evaluating cybersecurity, **there is virtually no overlap in quantitative benchmarks**. Each company has developed or adopted its own unique set:

- **OpenAI**: Custom CTF + CVE-Bench + OpenAI Cyber Range + Irregular/Pattern Labs
- **Anthropic**: Cybench + CyberGym + CMU Cyber Range + Real CTF competitions + ART benchmark
- **Google**: InterCode-CTF (retired) + In-house CTF (retired) + Key Skills Benchmark + Pattern Labs + TAP/Beam Search
- **xAI**: Cybench (spelled "CyBench") + WMDP-Cyber + AgentHarm + AgentDojo + MASK + MakeMeSay + Sycophancy

This makes **direct cross-company comparison nearly impossible** — which is exactly the problem this awesome repo aims to solve.

---

## 8. Documentation Maturity

| | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| **First cyber-specific benchmark** | GPT-4o (Aug 2024) | Claude 3 (Mar 2024) | Phuong et al. (Mar 2024) | Grok 4 (Aug 2025) |
| **Total documents w/ cyber benchmarks** | 21 | 24 | 25+ | 9 |
| **System card page count (latest)** | ~50-80p | 212p (Opus 4.6) | ~30-50p | ~20-30p |
| **Open-sources evals?** | No | No | Yes (In-house CTF via Inspect) | No (uses UK AISI Inspect) |
| **Real-world threat intel published?** | No | Yes (GTG-1002 espionage) | Yes (12,000+ incidents via GTI) | No |
| **Specialized cyber model?** | Aardvark (private beta) | — | Sec-Gemini v1 | — |
| **CAISI assessment?** | Yes (GPT-5.3-Codex) | Yes (Opus 4.6) | — | — |

---

## 9. Timeline

| Date | OpenAI | Anthropic | Google | xAI |
|---|---|---|---|---|
| 2023.03 | GPT-4: Low | — | — | — |
| 2023.07 | — | Claude 2: qualitative | — | — |
| 2023.11 | — | — | — | Grok-1: no cyber eval |
| 2023.12 | — | — | Gemini 1.0: rudimentary (InterCode-CTF 29%) | — |
| 2024.03 | — | Claude 3: ASL-2 | Phuong et al.: early warning | — |
| 2024.06 | — | Claude 3.5 Sonnet: ASL-2 | — | — |
| 2024.08 | GPT-4o: Low (1% Professional CTF) | — | — | — |
| 2024.09 | o1-preview/o1-mini: Low | — | — | — |
| 2024.10 | — | Claude 3.5 Haiku/Sonnet (upgraded): ASL-2 | — | — |
| 2024.12 | o1: Low (13% Professional CTF) | — | — | — |
| 2025.01 | o3-mini: Low (HS 61%, Coll 21%) | — | — | — |
| 2025.02 | Deep Research: **Medium** (70% Pro w/ browse) | Claude 3.7 Sonnet: ASL-2 (Cybench 35.9%) | — | xAI RMF Draft |
| 2025.03 | — | — | arXiv:2503.11917 (Gemini 2.0 Flash: 11/50 Pattern Labs) | — |
| 2025.04 | o3/o4-mini: Below High (o3 ~59% Pro CTF) | — | Gemini 2.5 Pro Preview: CCL alert; Sec-Gemini v1 (~86.5% CTI-MCQ) | — |
| 2025.05 | — | Claude Opus 4: **ASL-3** (first) | Stealth/SA paper; Prompt Injection paper | — |
| 2025.06 | — | — | Gemini 2.5 Flash/Pro final model cards | — |
| 2025.07 | ChatGPT Agent: refactored CTF set | — | Gemini 2.5 Technical Report | — |
| 2025.08 | GPT-5: Below High (~27% CTF, 0/30 Cyber Range) | Opus 4.1: ASL-3; GTG-1002 espionage report | Gemini 2.5 Deep Think: 13/13 in-house CTF | Grok 4: below human pro (WMDP-Cyber 79%, CyBench 43%) |
| 2025.09 | GPT-5-Codex: Below High (~50% CTF) | Sonnet 4.5: ASL-3 (Cybench 76.5%, Equifax 2/5) | — | Grok 4 Fast: WMDP-Cyber 81.4%, CyBench 30% |
| 2025.10 | — | Haiku 4.5: ASL-2 | FSF v3.0 published | — |
| 2025.11 | GPT-5.1-Codex-Max: Below High (76% CTF, 80% CVE-Bench) | Opus 4.5: ASL-3 (Cybench 82%, CyberGym 51%) | Gemini 3 Pro: Key Skills v1 11/12, v2 0/13 | Grok 4.1: WMDP-Cyber 84%, CyBench 39%; Grok 4.1 Fast announced (no card) |
| 2025.12 | GPT-5.2-Codex: Below High (88% CTF, 87% CVE-Bench) | — | Gemini 3 Flash | xAI FAIF published |
| 2026.01 | — | Cyber Ranges Report (Sonnet 4.5) | — | — |
| 2026.02 | GPT-5.3-Codex: **HIGH** (88% CTF, 90% CVE-Bench, 80% Cyber Range) | Opus 4.6: ASL-3 (Cybench 93%, CyberGym 66.6%); Sonnet 4.6: **ASL-3** (Cybench 90%, CyberGym 65.2%) | Gemini 3.1 Pro: CCL alert, not met; Deep Think worse than standard on cyber | — |

---

## 10. Sources

### OpenAI
- [Preparedness Framework v2](https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf)
- [GPT-4 System Card](https://cdn.openai.com/papers/gpt-4-system-card.pdf) | [Technical Report](https://cdn.openai.com/papers/gpt-4.pdf)
- [GPT-4o System Card](https://cdn.openai.com/gpt-4o-system-card.pdf)
- [o1 System Card (Sep 2024)](https://cdn.openai.com/o1-system-card.pdf)
- [o1 System Card (Dec 2024)](https://cdn.openai.com/o1-system-card-20241205.pdf)
- [Operator System Card](https://cdn.openai.com/operator_system_card.pdf)
- [o3-mini System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf)
- [Deep Research System Card](https://cdn.openai.com/deep-research-system-card.pdf)
- [GPT-4.5 System Card](https://cdn.openai.com/gpt-4-5-system-card-2272025.pdf)
- [o3/o4-mini System Card](https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf)
- [Codex Addendum](https://cdn.openai.com/pdf/8df7697b-c1b2-4222-be00-1fd3298f351d/codex_system_card.pdf)
- [o3 Operator Addendum](https://cdn.openai.com/pdf/4375e605-f9a6-438d-bcc8-190599c183a6/o3_cua_system_card.pdf)
- [ChatGPT Agent System Card](https://cdn.openai.com/pdf/6bcccca6-3b64-43cb-a66e-4647073142d7/chatgpt_agent_system_card_launch.pdf)
- [GPT-5 System Card](https://cdn.openai.com/gpt-5-system-card.pdf) | [arXiv:2601.03267](https://arxiv.org/abs/2601.03267)
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
- [Framework for Evaluating Emerging Cyberattack Capabilities](https://arxiv.org/abs/2503.11917)

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
