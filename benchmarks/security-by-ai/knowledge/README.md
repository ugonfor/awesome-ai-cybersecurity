# Security BY AI — Knowledge Benchmarks

> Evaluating AI's cybersecurity domain knowledge: threat intelligence, vulnerability classification, killchain understanding.

---

### [WMDP-Cyber](https://www.wmdp.ai/)
- **Category**: Security BY AI > Knowledge
- **Created by**: Center for AI Safety (CAIS)
- **Used by**: xAI
- **Scale**: Multiple-choice questions covering cyber killchain (recon, weaponization, exploitation, post-exploitation)
- **Dataset**: Open
- **Reference**: [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/abs/2403.03218)
- **Summary**: Multiple-choice cybersecurity knowledge benchmark covering the full cyber killchain, originally designed for measuring dual-use knowledge.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 79% | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4 Fast | 81.4% | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 | 87% (WMDP-Bio; WMDP-Cyber score not separately reported) | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### MC Cybersecurity Knowledge
- **Category**: Security BY AI > Knowledge
- **Created by**: OpenAI
- **Used by**: OpenAI
- **Scale**: Internal multiple-choice evaluation
- **Dataset**: Closed
- **Summary**: OpenAI's internal multiple-choice cybersecurity knowledge assessment.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | o3-mini | 53% | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |
  | o1 | 59% | 2025.01 | [System Card](https://cdn.openai.com/o3-mini-system-card-feb10.pdf) |

---

### CTI-MCQ (Sec-Gemini)
- **Category**: Security BY AI > Knowledge > Threat Intelligence
- **Created by**: Rochester Institute of Technology ([CTI-Bench](https://github.com/xashru/cti-bench) project)
- **Used by**: Google (Sec-Gemini)
- **Scale**: Threat intelligence multiple-choice questions
- **Dataset**: Closed
- **Reference**: [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html)
- **Summary**: Cyber Threat Intelligence multiple-choice benchmark measuring knowledge of threat actors, campaigns, TTPs, and indicators.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Sec-Gemini v1 | +11% over competitors | 2025.04 | [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

---

### CTI-RCM (Sec-Gemini)
- **Category**: Security BY AI > Knowledge > Vulnerability Classification
- **Created by**: Rochester Institute of Technology ([CTI-Bench](https://github.com/xashru/cti-bench) project)
- **Used by**: Google (Sec-Gemini)
- **Scale**: Root cause to CWE mapping tasks
- **Dataset**: Closed
- **Reference**: [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html)
- **Summary**: Root Cause Mapping benchmark evaluating ability to map vulnerability root causes to CWE (Common Weakness Enumeration) categories.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Sec-Gemini v1 | +10.5% over competitors | 2025.04 | [Blog](https://security.googleblog.com/2025/04/google-launches-sec-gemini-v1-new.html) |

---

## Academic Benchmarks (Community-Driven)

> The following knowledge benchmarks originate from the academic community and are not primarily used in the four major vendors' official model evaluations.

---

### [SecBench](https://github.com/secbench-git/SecBench)
- **Category**: Security BY AI > Knowledge > Multi-dimensional
- **Created by**: Academic researchers (secbench-git)
- **Used by**: Academic community
- **Scale**: 44,823 MCQs + 3,087 short-answer questions across 9 cybersecurity sub-domains and 2 difficulty levels; bilingual (EN/ZH)
- **Dataset**: Open ([HuggingFace](https://huggingface.co/datasets/secbench-hf/SecBench))
- **Reference**: [SecBench: A Comprehensive Multi-Dimensional Benchmarking Dataset for LLMs in Cybersecurity](https://arxiv.org/abs/2412.20787)
- **Summary**: Largest cybersecurity knowledge benchmark (47,910 questions total) evaluating LLMs across multi-level (knowledge retention vs logical reasoning), multi-language (EN/ZH), multi-form (MCQ/SAQ), and multi-domain dimensions; shows LLMs perform better on knowledge retention than logical reasoning.

---

### [CyberMetric](https://github.com/cybermetric/CyberMetric)
- **Category**: Security BY AI > Knowledge > Domain Evaluation
- **Created by**: Academic researchers (Tihanyi, Ferrag et al.)
- **Used by**: Academic community (highest citations among cybersec MCQ benchmarks as of mid-2025)
- **Scale**: 10,000 questions across 4 variants (CyberMetric-80/500/2000/10000); 9 domains including cryptography, network security, IoT, cloud, pen testing
- **Dataset**: Open
- **Reference**: [CyberMetric: A Benchmark Dataset based on Retrieval-Augmented Generation for Evaluating LLMs in Cybersecurity Knowledge](https://arxiv.org/abs/2402.07688)
- **Summary**: RAG-generated, human-validated (200+ expert hours) cybersecurity knowledge benchmark; top LLMs (GPT-4o, Gemini Pro) outperform human professionals on CyberMetric-80. IEEE CSR 2024.

---

### [SecQA](https://huggingface.co/datasets/zefang-liu/secqa)
- **Category**: Security BY AI > Knowledge > Educational
- **Created by**: Zefang Liu (individual researcher)
- **Used by**: Academic community
- **Scale**: 242 multiple-choice questions in 2 sets: v1 (127 questions, introductory) and v2 (115 questions, advanced)
- **Dataset**: Open ([HuggingFace](https://huggingface.co/datasets/zefang-liu/secqa))
- **Reference**: [SecQA: A Concise Question-Answering Dataset for Evaluating Large Language Models in Computer Security](https://arxiv.org/abs/2312.15838)
- **Summary**: Compact, textbook-derived (GPT-4 generated from "Computer Systems Security") cybersecurity QA benchmark; strong alignment with learning objectives; named Top 8 LLM Benchmark for Cybersecurity by Infosecurity Europe.

---

### [SecEval](https://github.com/XuanwuAI/SecEval)
- **Category**: Security BY AI > Knowledge > Foundation Model Evaluation
- **Created by**: Tencent Security Xuanwu Lab
- **Used by**: Academic community
- **Scale**: ~2,100 multiple-choice questions across 9 domains (software security, application security, system security, web security, cryptography, memory safety, network security, pen testing)
- **Dataset**: Open ([HuggingFace](https://huggingface.co/datasets/XuanwuAI/SecEval))
- **Summary**: First benchmark specifically designed for evaluating cybersecurity knowledge in foundation models; GPT-4 pipeline generated from OWASP, MITRE ATT&CK, CWE, academic texts, and vendor documentation.

---

### [CTI-Bench](https://github.com/xashru/cti-bench)
- **Category**: Security BY AI > Knowledge > Cyber Threat Intelligence
- **Created by**: Rochester Institute of Technology
- **Used by**: Academic community
- **Scale**: Multiple datasets: CTI-MCQ (knowledge), CTI-RCM (CVE-to-CWE mapping), CTI-VSP (CVSS scoring), CTI-TAA (threat actor attribution)
- **Dataset**: Open ([HuggingFace](https://huggingface.co/datasets/AI4Sec/cti-bench))
- **Reference**: [CTIBench: A Benchmark for Evaluating LLMs in Cyber Threat Intelligence](https://arxiv.org/abs/2406.07599)
- **Summary**: Practical CTI benchmark evaluating knowledge of NIST/MITRE standards, CWE classification, CVSS scoring, and threat attribution from public reports. NeurIPS 2024 Spotlight.

---

### [SECURE](https://arxiv.org/abs/2405.20441)
- **Category**: Security BY AI > Knowledge > ICS/Critical Infrastructure
- **Created by**: Argonne National Laboratory / UChicago
- **Used by**: Academic community
- **Scale**: 6 datasets focused on ICS: MAET (MITRE ATT&CK extraction), CWET (CWE extraction), KCV (CVE knowledge), VOOD (vulnerability OOD), RERT (risk evaluation reasoning), CPST (CVSS problem solving)
- **Dataset**: Partial
- **Reference**: [SECURE: Benchmarking Large Language Models for Cybersecurity](https://arxiv.org/abs/2405.20441)
- **Summary**: ICS-focused cybersecurity advisory benchmark evaluating LLMs on knowledge extraction, understanding, and reasoning using industry-standard sources; 7 models evaluated including GPT-4, Llama 3, Gemini Pro.

---

### [CS-Eval](https://github.com/CS-EVAL/CS-Eval)
- **Category**: Security BY AI > Knowledge > Comprehensive
- **Created by**: Academic researchers
- **Used by**: Academic community
- **Scale**: 42 subcategories across 11 top-level categories; 3 cognitive levels (knowledge, ability, application)
- **Dataset**: Open
- **Reference**: [CS-Eval: A Comprehensive Large Language Model Benchmark for CyberSecurity](https://arxiv.org/abs/2411.16239)
- **Summary**: Comprehensive cybersecurity benchmark spanning academia and industry topics; GPT-4 generally excels but other models outperform in specific subcategories; tracks LLM improvement over time.

---

### [WMDP (Weapons of Mass Destruction Proxy)](https://github.com/centerforaisafety/wmdp)
- **Category**: Security BY AI > Knowledge > Hazardous Knowledge (dual-use)
- **Created by**: Center for AI Safety (CAIS), Scale AI, 20+ academic institutions
- **Used by**: xAI (WMDP-Cyber subset), academic community
- **Scale**: 3,668 multiple-choice questions across 3 domains: biosecurity, cybersecurity, chemical security
- **Dataset**: Open (filtered to remove sensitive info)
- **Reference**: [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/abs/2403.03218)
- **Summary**: Proxy measurement of hazardous knowledge in LLMs; serves dual purpose as evaluation benchmark and unlearning target (with RMU method). ICML 2024.
