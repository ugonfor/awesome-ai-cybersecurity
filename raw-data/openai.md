# OpenAI: System Cards, Model Cards, and Technical Reports

## Cybersecurity Evaluation Framework

OpenAI evaluates cybersecurity risks under its **Preparedness Framework** (v1: 2023, v2: April 2025). The framework tracks cybersecurity as a core risk category with thresholds: **Low**, **Medium**, **High**, **Critical**.

**High** = model automates end-to-end cyber operations against hardened targets, or automates discovery/exploitation of operationally relevant zero-day vulnerabilities.

### Primary Benchmarks

| Benchmark | Description |
|---|---|
| **CTF Challenges** | Offensive exercises at high-school/collegiate/professional levels (web exploit, RE, pwn, crypto, misc). Models use Kali Linux. |
| **CVE-Bench** | Exploit real-world web app vulnerabilities (actual CVEs). pass@1 metric. |
| **Cyber Range** | Realistic multi-machine network scenarios testing end-to-end attack capabilities. |
| **Expert Red Teaming** | Qualitative assessments by external cybersecurity experts. |

---

## Documents

### 1. GPT-4 System Card

- **Date**: March 23, 2023
- **URL**: https://cdn.openai.com/papers/gpt-4-system-card.pdf
- **Models**: GPT-4
- **Cyber Risk Level**: Low
- **Benchmarks**: Expert Red Teaming (50+ external experts), qualitative cyber assessment
- **Finding**: Not vastly superior to previous LLMs; useful for social engineering subtasks

### 2. GPT-4 Technical Report

- **Date**: March 14, 2023
- **URL**: https://cdn.openai.com/papers/gpt-4.pdf | arXiv:2303.08774
- **Models**: GPT-4
- **Benchmarks**: References System Card evaluations, model-assisted safety pipeline

### 3. GPT-4o System Card

- **Date**: August 8, 2024
- **URL**: https://cdn.openai.com/gpt-4o-system-card.pdf | arXiv:2410.21276
- **Blog**: https://openai.com/index/gpt-4o-system-card/
- **Models**: GPT-4o (GPT-4o mini shares mitigations but not separately evaluated)
- **Cyber Risk Level**: Low
- **Benchmarks**: CTF (172 challenges, 4 categories, 30 rounds tool use, 10 attempts/task)
  - High-school: **19%**, Collegiate: **0%**, Professional: **1%**
- **Finding**: Does not meet medium risk threshold

### 4. OpenAI o1 System Card (September 2024)

- **Date**: September 12, 2024
- **URL**: https://cdn.openai.com/o1-system-card.pdf
- **Blog**: https://openai.com/index/openai-o1-system-card/
- **Models**: o1-preview, o1-mini
- **Cyber Risk Level**: Low
- **Benchmarks**: CTF (5 categories, 60 rounds tool use, 12 attempts/task)
  - o1-preview: HS **26.7%**, Collegiate **0%**, Professional **2.5%**
  - o1-mini: HS **28.7%**, Collegiate **0%**, Professional **3.9%**
- **Notable**: o1-preview exhibited reward hacking on cybersecurity tasks

### 5. OpenAI o1 System Card (December 2024)

- **Date**: December 5, 2024
- **URL**: https://cdn.openai.com/o1-system-card-20241205.pdf | arXiv:2412.16720
- **Models**: o1, o1-preview, o1-mini
- **Cyber Risk Level**: Low
- **Benchmarks**: CTF (updated methodology)
  - o1: HS **46.0%**, Collegiate **13.0%**, Professional **13.0%**
- **Note**: o1-pro covered under o1 family (same base model + enhanced compute)

### 6. Operator System Card

- **Date**: January 23, 2025
- **URL**: https://cdn.openai.com/operator_system_card.pdf
- **Blog**: https://openai.com/index/operator-system-card/
- **Models**: Operator (CUA based on GPT-4o)
- **Cyber Risk Level**: Low (inherited from GPT-4o)
- **Benchmarks**: Prompt Injection (99% recall on 77 attempts), Harmful Task Refusal (97%)

### 7. OpenAI o3-mini System Card

- **Date**: January 31, 2025 (updated February 10, 2025)
- **URL**: https://cdn.openai.com/o3-mini-system-card-feb10.pdf
- **Blog**: https://openai.com/index/o3-mini-system-card/
- **Models**: o3-mini
- **Cyber Risk Level**: Low
- **Benchmarks**: CTF (5 categories)
  - o3-mini: HS **61%**, Collegiate **21%**
  - MC cybersecurity knowledge: o3-mini **53%**, o1 **59%** (18% uplift over GPT-4o)

### 8. Deep Research System Card

- **Date**: February 25, 2025
- **URL**: https://cdn.openai.com/deep-research-system-card.pdf
- **Blog**: https://openai.com/index/deep-research-system-card/
- **Models**: Deep Research (o3-based + web browsing)
- **Cyber Risk Level**: **Medium** (first OpenAI model at this level)
- **Benchmarks**: CTF
  - Without browsing: HS **82%**, Collegiate **55%**, Professional **47%**
  - With browsing: HS **92%**, Collegiate **91%**, Professional **70%**
  - Prompt Injection evaluation for web browsing

### 9. GPT-4.5 System Card

- **Date**: February 27, 2025
- **URL**: https://cdn.openai.com/gpt-4-5-system-card-2272025.pdf
- **Blog**: https://openai.com/index/gpt-4-5-system-card/
- **Models**: GPT-4.5
- **Cyber Risk Level**: Low
- **Benchmarks**: CTF (same framework as GPT-4o/o1)

### 10. OpenAI o3 and o4-mini System Card

- **Date**: April 16, 2025
- **URL**: https://cdn.openai.com/pdf/2221c875-02dc-4789-800b-e7758f3722c1/o3-and-o4-mini-system-card.pdf
- **Blog**: https://openai.com/index/o3-o4-mini-system-card/
- **Models**: o3, o4-mini
- **Cyber Risk Level**: Below High (first evaluated under Preparedness Framework v2)
- **Benchmarks**: CTF + Cyber Range + Irregular (Pattern Labs) external eval
  - o3: HS **89%**, Collegiate **68%**, Professional **59%** (pass@12)
  - o4-mini: HS **80%**, Collegiate **55%**, Professional **41%** (pass@12)
  - Cyber Range: 0% unaided for both models (2 scenarios)
  - Note: o1 scored 13% on Dec 2024 CTF set; the refactored set used here gives different baselines

### 11. Codex Addendum (o3/o4-mini)

- **Date**: May 16, 2025
- **URL**: https://cdn.openai.com/pdf/8df7697b-c1b2-4222-be00-1fd3298f351d/codex_system_card.pdf
- **Blog**: https://openai.com/index/o3-o4-mini-codex-system-card-addendum/
- **Models**: codex-1 (o3 optimized for SWE)
- **Cyber Risk Level**: Below High (inherits o3/o4-mini)
- **Benchmarks**: Malware-related benchmark (synthetic, large-scale, dual-use prompts)

### 12. o3 Operator Addendum

- **Date**: 2025
- **URL**: https://cdn.openai.com/pdf/4375e605-f9a6-438d-bcc8-190599c183a6/o3_cua_system_card.pdf
- **Blog**: https://openai.com/index/o3-o4-mini-system-card-addendum-operator-o3/
- **Models**: o3 Operator (CUA)
- **Cyber Risk Level**: Below High
- **Benchmarks**: Preparedness Framework evals (cyber, persuasion, CBRN, autonomy)

### 13. ChatGPT Agent System Card

- **Date**: July 17, 2025
- **URL**: https://cdn.openai.com/pdf/6bcccca6-3b64-43cb-a66e-4647073142d7/chatgpt_agent_system_card_launch.pdf
- **Models**: ChatGPT Agent
- **Benchmarks**:
  - Refactored CTF set (updated with recent CTFs, rebalanced difficulty)
  - Cyber Range: "Online Retailer" scenario (Linux VM, Windows VM, CI/CD, web server, cloud storage)
  - Three-skill framework: exploit discovery, end-to-end attack automation, consistency/scalability

### 14. GPT-5 System Card

- **Date**: August 13, 2025
- **URL**: https://cdn.openai.com/gpt-5-system-card.pdf | arXiv:2601.03267
- **Blog**: https://openai.com/index/gpt-5-system-card/
- **Models**: GPT-5 (gpt-5-thinking, gpt-5-thinking-mini)
- **Cyber Risk Level**: Below High
- **Benchmarks** (two core evaluations):
  1. Professional CTF (pass@12): ~**27%**
  2. Cyber Range: expanded to 5 scenarios
  - Note: CVE-Bench was NOT introduced in GPT-5; it first appears in the GPT-5.1-Codex-Max card.

### 15. GPT-5-Codex Addendum

- **Date**: September 15, 2025
- **URL**: https://cdn.openai.com/pdf/97cc5669-7a25-4e63-b15f-5fd5bdc4d149/gpt-5-codex-system-card.pdf
- **Blog**: https://openai.com/index/gpt-5-system-card-addendum-gpt-5-codex/
- **Models**: GPT-5-Codex
- **Benchmarks**: Professional CTFs, CVE-Bench, Cyber Range. "Sharp jump" in capability.

### 16. GPT-5.1-Codex-Max System Card

- **Date**: November 18, 2025
- **URL**: https://cdn.openai.com/pdf/2a7d98b1-57e5-4147-8d0e-683894d782ae/5p1_codex_max_card_03.pdf
- **Blog**: https://openai.com/index/gpt-5-1-codex-max-system-card/
- **Models**: GPT-5.1-Codex-Max
- **Cyber Risk Level**: Below High (most cyber-capable at time)
- **Benchmarks**:
  - Professional CTF: **76%** (up from 27%)
  - Cyber Range: Network Attack **37%**, Vuln Discovery **41%**, Evasion **43%**
  - Solved 17/18 easy, 9/17 medium, 0/6 hard

### 17. GPT-5.2 System Card Update

- **Date**: December 11, 2025
- **URL**: https://cdn.openai.com/pdf/3a4153c8-c748-4b71-8e31-aecbde944f8d/oai_5_2_system-card.pdf
- **Blog**: https://openai.com/index/gpt-5-system-card-update-gpt-5-2/
- **Models**: GPT-5.2
- **Cyber Risk Level**: Below High
- **Benchmarks**: Professional CTFs, CVE-Bench, Cyber Range
- **Notable**: Introduced "safe-completions" for dual-use cybersecurity queries

### 18. GPT-5.2-Codex Addendum

- **Date**: December 18, 2025
- **URL**: https://cdn.openai.com/pdf/ac7c37ae-7f4c-4442-b741-2eabdeaf77e0/oai_5_2_Codex.pdf
- **Blog**: https://openai.com/index/gpt-5-2-codex-system-card/
- **Models**: GPT-5.2-Codex
- **Cyber Risk Level**: Below High (strongest at time)
- **Benchmarks**:
  - Professional CTFs: strongest at time of release
  - CVE-Bench: **87%**
  - "Current trends suggest models may cross High threshold in near future"

### 19. GPT-5.3-Codex System Card

- **Date**: February 5, 2026
- **URL**: https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf
- **Blog**: https://openai.com/index/gpt-5-3-codex-system-card/
- **Models**: GPT-5.3-Codex, GPT-5.3-Codex-Spark
- **Cyber Risk Level**: **HIGH (precautionary)** — "We do not have definitive evidence that this model reaches our High threshold, but are taking a precautionary approach." First OpenAI model at this level.
- **Benchmarks**:
  - First model to pass all thresholds across all three evaluations
  - CVE-Bench: **90%** (pass@1, 34/40 challenges, zero-day config)
  - Cyber Range: **80%** combined pass rate (12/15 scenarios; failed: EDR Evasion, CA/DNS Hijacking, Leaked Token)
  - Irregular External: Network Attack **86%**, Vuln D&E **72%**, Evasion **53%**
  - GPT-5.3-Codex-Spark: Below High

---

## Framework Documents

### 20. Preparedness Framework v2

- **Date**: April 15, 2025
- **URL**: https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf
- **Blog**: https://openai.com/index/updating-our-preparedness-framework/
- Three Tracked Categories: Cybersecurity, Bio/Chemical, AI Self-improvement
- Two thresholds: **High** and **Critical**

### 21. Strengthening Cyber Resilience Report

- **Date**: December 2025
- **URL**: https://openai.com/index/strengthening-cyber-resilience/
- CTF progression: 27% (GPT-5) → 76% (GPT-5.1-Codex-Max)
- CVE-Bench: 87% (GPT-5.2-Codex)
- Introduces **Aardvark** (agentic security researcher)
- **Frontier Risk Council**, **Trusted Access for Cyber** program

---

## Cyber Risk Progression

| Model | Date | Risk Level | Professional CTF |
|---|---|---|---|
| GPT-4 | 2023.03 | Low | Qualitative only |
| GPT-4o | 2024.08 | Low | 1% |
| o1-preview | 2024.09 | Low | 2.5% |
| o1-mini | 2024.09 | Low | 3.9% |
| o1 | 2024.12 | Low | 13% |
| o3-mini | 2025.01 | Low | HS 61%, Coll 21% |
| Deep Research (no browse) | 2025.02 | Medium | 47% |
| Deep Research (w/ browse) | 2025.02 | Medium | 70% |
| GPT-4.5 | 2025.02 | Low | — |
| o3 | 2025.04 | Below High | ~58% |
| GPT-5 | 2025.08 | Below High | ~27% |
| GPT-5.1-Codex-Max | 2025.11 | Below High | ~76% |
| GPT-5.2-Codex | 2025.12 | Below High | CVE-Bench 87% |
| GPT-5.3-Codex | 2026.02 | **HIGH** | All thresholds passed |

## Notes

- **GPT-3.5**: No standalone system card with cybersecurity benchmarks
- **GPT-4o mini**: No separate system card; shares GPT-4o mitigations
- **o1-pro**: Covered under o1 System Card (Dec 2024); no separate cyber eval
- **US/UK AISI Joint Test for o1**: https://www.nist.gov/system/files/documents/2024/12/18/US_UK_AI%20Safety%20Institute_%20December_Publication-OpenAIo1.pdf
