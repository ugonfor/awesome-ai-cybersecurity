# Google DeepMind / Gemini: Technical Reports, Model Cards, and Safety Evaluations

## Cybersecurity Evaluation Framework

Google evaluates cybersecurity under the **Frontier Safety Framework (FSF)** with **Critical Capability Levels (CCLs)**.

**Cyber Uplift Level 1**: "The model can be used to significantly assist with high impact cyber attacks, resulting in overall cost/resource reductions of an order of magnitude or more."

### Primary Benchmarks

| Benchmark | Difficulty | Description |
|---|---|---|
| **InterCode-CTF** | Easy | 76 CTF challenges (largely saturated) |
| **In-house CTF Suite** | Medium | 13 GDM-built challenges (web, exploits, DB, privesc, passwords) |
| **Hack the Box** | Hard | Professional-level CTF challenges |
| **Key Skills Benchmark** | Mixed | Recon, tool dev, tool use, OPSEC (MITRE ATT&CK aligned) |
| **Pattern Labs External CTFs** | Mixed | 50 non-public challenges (anti-contamination) |
| **CTI-MCQ / CTI-RCM** | N/A | Threat intelligence knowledge (Sec-Gemini) |

---

## Technical Reports

### 1. Gemini 1.0 Technical Report

- **Date**: December 2023
- **URL**: https://arxiv.org/abs/2312.11805
- **Models**: Gemini 1.0 Ultra, Pro, Nano
- **Benchmarks**: Dangerous capabilities evals (persuasion, cybersecurity, self-proliferation, self-reasoning). Rudimentary capabilities; moderate threats in deception and cybersecurity.

### 2. Gemini 1.5 Technical Report

- **Date**: February 2024
- **URL**: https://arxiv.org/abs/2403.05530 | [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_v1_5_report.pdf)
- **Models**: Gemini 1.5 Pro, Flash
- **Benchmarks**: Safety evaluations (SFT/RLHF mitigations), safety violation rate comparisons vs 1.0

### 3. Gemini 2.5 Technical Report

- **Date**: July 2025
- **URL**: https://arxiv.org/abs/2507.06261 | [PDF](https://storage.googleapis.com/deepmind-media/gemini/gemini_v2_5_report.pdf)
- **Models**: Gemini 2.5 Pro, Flash, 2.0 Flash, 2.0 Pro (experimental)
- **Benchmarks** (most comprehensive Gemini cyber report):
  - InterCode-CTF: 73-76/76 (saturated)
  - In-house CTF: Gemini 2.5 Deep Think 13/13
  - Hack the Box: Gemini 2.5 Deep Think 3/13
  - Key Skills Benchmark
  - Pattern Labs External CTFs: 2.0 Flash 11/50
  - FSF: Cyber Uplift Level 1 CCL alert threshold reached, CCL not met
  - Indirect Prompt Injection: TAP 99.8% → 53.6% (2.0 → 2.5)

---

## Model Cards

### 4. Gemini 1.0 Model Card

- **Date**: December 2023
- **URL**: https://storage.googleapis.com/deepmind-media/gemini/gemini_1_report.pdf (page 71)
- **Models**: Gemini 1.0 Ultra, Pro, Nano

### 5. Gemini 1.5 Model Card

- **Date**: 2024
- **URL**: https://storage.googleapis.com/deepmind-media/gemini/gemini_v1_5_report.pdf (page 105)
- **Models**: Gemini 1.5 Pro, Flash

### 6. Gemini 2.0 Flash-Lite Model Card

- **Date**: April 10, 2025
- **URL**: https://modelcards.withgoogle.com/assets/documents/gemini-2-flash-lite.pdf
- **Models**: Gemini 2.0 Flash-Lite

### 7. Gemini 2.0 Flash Model Card

- **Date**: April 15, 2025
- **URL**: https://modelcards.withgoogle.com/assets/documents/gemini-2-flash.pdf
- **Models**: Gemini 2.0 Flash
- **Benchmarks**: Pattern Labs CTF (11/50), FSF evals

### 8. Gemini 2.5 Pro Preview Model Card

- **Date**: April 16, 2025
- **URL**: https://storage.googleapis.com/model-cards/documents/gemini-2.5-pro-preview.pdf
- **Models**: Gemini 2.5 Pro Preview
- **Benchmarks**: FSF (InterCode-CTF, in-house CTF, HTB). CCL alert threshold reached.

### 9. Gemini 2.5 Flash Preview Model Card

- **Date**: June 6, 2025
- **URL**: https://storage.googleapis.com/model-cards/documents/gemini-2.5-flash-preview.pdf
- **Models**: Gemini 2.5 Flash Preview

### 10. Gemini 2.5 Flash Model Card

- **Date**: June 26, 2025
- **URL**: https://modelcards.withgoogle.com/assets/documents/gemini-2.5-flash.pdf | [Updated](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Flash-Model-Card.pdf)
- **Models**: Gemini 2.5 Flash

### 11. Gemini 2.5 Pro Model Card

- **Date**: June 27, 2025
- **URL**: https://modelcards.withgoogle.com/assets/documents/gemini-2.5-pro.pdf
- **Models**: Gemini 2.5 Pro
- **Benchmarks**: Comprehensive FSF evals, in-house CTF open-sourced via UK AISI Inspect, N=30-50 attempts

### 12. Gemini 2.5 Deep Think Model Card

- **Date**: August 1, 2025
- **URL**: https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Deep-Think-Model-Card.pdf
- **Models**: Gemini 2.5 Deep Think
- **Benchmarks**: InterCode-CTF 73/76, In-house CTF **13/13** (strongest), HTB 3/13. CCL alert for both Cyber and CBRN.

### 13. Gemini 2.5 Flash-Lite Model Card

- **Date**: September 26, 2025
- **URL**: https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Flash-Lite-Model-Card.pdf
- **Models**: Gemini 2.5 Flash-Lite

### 14. Gemini 2.5 Computer Use Model Card

- **Date**: October 7, 2025
- **URL**: https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-2-5-Computer-Use-Model-Card.pdf
- **Models**: Gemini 2.5 Computer Use
- **Benchmarks**: Agent-specific risks (adversarial misuse, failure modes, prompt injections in web)

### 15. Gemini 3 Pro Model Card

- **Date**: November 18, 2025
- **URL**: https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-Pro-Model-Card.pdf
- **Models**: Gemini 3 Pro
- **Benchmarks**: FSF report reference. New harder realistic challenges (end-to-end attacks). CCL alert reached, CCL not met.

### 16. Gemini 3 Flash Model Card

- **Date**: December 17, 2025
- **URL**: https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-Flash-Model-Card.pdf
- **Models**: Gemini 3 Flash

### 17. Gemini 3.1 Pro Model Card

- **Date**: February 19, 2026
- **URL**: https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf
- **Models**: Gemini 3.1 Pro
- **Benchmarks**: FSF (Deep Think mode focus). Cyber Uplift Level 1 alert threshold, CCL not reached. Increased cyber capabilities vs 3 Pro.

---

## FSF Reports

### 18. Gemini 3 Pro FSF Report

- **Date**: November 2025
- **URL**: https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf
- **Models**: Gemini 3 Pro (with 2.5 comparisons)
- **Benchmarks** (most detailed standalone cyber eval):
  - InterCode-CTF: saturated
  - In-house CTF: significantly stronger than 2.5
  - HTB: **11/12** (vs 2.5's 6/12)
  - Key Skills: almost all hard challenges completed
  - New realistic multi-stage attack scenarios
  - MITRE ATT&CK and Unified Kill Chain aligned

### 19. FSF v1.0

- **Date**: May 2024
- **URL**: https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/introducing-the-frontier-safety-framework/fsf-technical-report.pdf

### 20. FSF v3.0

- **Date**: October 2025
- **URL**: https://storage.googleapis.com/deepmind-media/DeepMind.com/Blog/strengthening-our-frontier-safety-framework/frontier-safety-framework_3.pdf
- Four risk domains: CBRN, cybersecurity, ML R&D, harmful manipulation/misalignment

---

## Standalone Papers

### 21. Evaluating Frontier Models for Dangerous Capabilities (Phuong et al.)

- **Date**: March 20, 2024
- **URL**: https://arxiv.org/abs/2403.13793
- **Models**: Gemini 1.0 Pro, Ultra
- **Content**: Foundational paper. 13 in-house CTF challenges. ReAct agent. Open-source: github.com/google-deepmind/dangerous-capability-evaluations

### 22. Evaluating Frontier Models for Stealth and Situational Awareness

- **Date**: May 2, 2025
- **URL**: https://arxiv.org/abs/2505.01420
- **Models**: Gemini 2.5 Pro/Flash, GPT-4o, o1, Claude 3.7 Sonnet
- **Content**: 5 stealth evals + 11 situational awareness evals

### 23. Framework for Evaluating Emerging Cyberattack Capabilities

- **Date**: March 14, 2025
- **URL**: https://arxiv.org/abs/2503.11917
- **Models**: Gemini 2.0 Flash (experimental) + others
- **Content**: End-to-end attack chain, 12,000+ real-world incidents, 50 new challenges

### 24. Defending Gemini Against Indirect Prompt Injections

- **Date**: May 18, 2025
- **URL**: https://arxiv.org/abs/2505.14534 | [PDF](https://storage.googleapis.com/deepmind-media/Security%20and%20Privacy/Gemini_Security_Paper.pdf)
- **Models**: Gemini 2.0, 2.5 series
- **Content**: TAP attack success 99.8% → 53.6%, Automated Red Teaming (ART) framework

---

## Specialized Model

### 25. Sec-Gemini v1

- **Date**: April 2025
- **URL**: https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html | https://github.com/google/sec-gemini
- **Models**: Sec-Gemini v1
- **Benchmarks**:
  - CTI-MCQ: outperforms competitors by 11%+
  - CTI-RCM: outperforms by 10.5%+
  - Integrates Google Threat Intelligence, OSV, Mandiant data

---

## Key Milestones

- **No Gemini model has crossed Cyber Uplift Level 1 CCL** (as of Feb 2026)
- **CCL alert threshold** first reached with Gemini 2.5 Pro
- **Gemini 3 Pro HTB**: 11/12 (nearly doubled from 2.5's 6/12)
- Model cards indexed at: https://deepmind.google/models/model-cards/
