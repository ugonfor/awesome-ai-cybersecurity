# Security4AI — Model Robustness Benchmarks

> Protecting AI models from attacks: jailbreak resistance, prompt injection robustness, adversarial defense.

---

### Prompt Injection Evaluation
- **Category**: Security4AI > Model Robustness > Prompt Injection
- **Created by**: Multiple (each company has internal version)
- **Used by**: OpenAI, Anthropic, Google
- **Scale**: Varies by implementation
- **Dataset**: Closed (per company)
- **Summary**: Evaluates model robustness against prompt injection attacks that attempt to override system instructions or extract sensitive data.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Operator (GPT-4o) | 99% recall on 77 attempts | 2025.01 | [System Card](https://cdn.openai.com/operator_system_card.pdf) |
  | Claude Sonnet 4.6 | 0% attack success (coding w/ extended thinking) | 2026.02 | [System Card](https://anthropic.com/claude-sonnet-4-6-system-card) |

---

### [TAP (Tree of Attacks with Pruning)](https://arxiv.org/abs/2312.02119)
- **Category**: Security4AI > Model Robustness > Jailbreak
- **Created by**: Robust Intelligence (now part of Cisco)
- **Used by**: Google
- **Scale**: Automated attack generation pipeline
- **Dataset**: Open
- **Reference**: [Tree of Attacks: Jailbreaking Black-Box LLMs with Red-Teaming Language Models](https://arxiv.org/abs/2312.02119)
- **Summary**: Automated jailbreak attack method using tree-of-thought reasoning. Google tracks defense against TAP as a key robustness metric.
- **Results**:
  | Model | Attack Success Rate | Date | Source |
  |---|---|---|---|
  | Gemini 2.0 | 99.8% | 2025.05 | [Paper](https://arxiv.org/abs/2505.14534) |
  | Gemini 2.5 | 53.6% | 2025.05 | [Paper](https://arxiv.org/abs/2505.14534) |

---

### [AgentDojo](https://arxiv.org/abs/2406.13352)
- **Category**: Security4AI > Model Robustness > Prompt Injection > Agentic
- **Created by**: ETH Zurich
- **Used by**: xAI
- **Scale**: Prompt injection attacks in agentic tool-use settings
- **Dataset**: Open
- **Reference**: [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352)
- **Summary**: Evaluates AI agent robustness to prompt injection in realistic agentic workflows with tool use.
- **Results**:
  | Model | Attack Success Rate | Date | Source |
  |---|---|---|---|
  | Grok 4 Fast | 0-3% | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 | 0-3% | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### Jailbreak Robustness
- **Category**: Security4AI > Model Robustness > Jailbreak
- **Created by**: Multiple (internal evaluations)
- **Used by**: OpenAI, Anthropic
- **Scale**: Varies
- **Dataset**: Closed
- **Summary**: Testing model resistance to universal jailbreak techniques including prompt manipulation, persona switching, and encoding tricks.

---

### [Automated Red Teaming (ART)](https://arxiv.org/abs/2505.14534)
- **Category**: Security4AI > Model Robustness > Continuous Adversarial Evaluation
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: Continuous evaluation framework
- **Dataset**: Closed
- **Reference**: [Defending Gemini Against Indirect Prompt Injections](https://arxiv.org/abs/2505.14534)
- **Summary**: Continuous automated adversarial evaluation framework for testing Gemini's robustness against evolving attack techniques.

---

### Expert Red Teaming
- **Category**: Security4AI > Model Robustness > Manual Adversarial Evaluation
- **Created by**: Multiple (external security researchers)
- **Used by**: OpenAI, Anthropic, Google
- **Scale**: 50+ external experts (OpenAI); varies by company
- **Dataset**: Closed
- **Summary**: Qualitative adversarial testing by external cybersecurity experts, often including domain specialists in exploit development, social engineering, and network attacks.

---

## Academic Benchmarks (Community-Driven)

> The following benchmarks originate from the academic community and are not primarily used in the four major vendors' (OpenAI, Anthropic, Google, xAI) official model evaluations.

---

### [HarmBench](https://github.com/centerforaisafety/HarmBench)
- **Category**: Security4AI > Model Robustness > Jailbreak > Automated Red Teaming
- **Created by**: Center for AI Safety (CAIS)
- **Used by**: Academic community (widely adopted as de facto standard)
- **Scale**: 510 unique harmful behaviors across 4 functional categories; 18 red teaming methods evaluated against 33 target LLMs
- **Dataset**: Open
- **Reference**: [HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal](https://arxiv.org/abs/2402.04249)
- **Summary**: Standardized evaluation framework for comparing jailbreak attacks and defenses with reproducible metrics across models. Published at ICML 2024.

---

### [JailbreakBench](https://github.com/JailbreakBench/jailbreakbench)
- **Category**: Security4AI > Model Robustness > Jailbreak > Robustness Benchmark
- **Created by**: University of Pennsylvania, ETH Zurich, EPFL
- **Used by**: Academic community
- **Scale**: 100 distinct misuse behaviors (JBB-Behaviors dataset) + 100 matching benign behaviors; includes leaderboard tracking attacks and defenses
- **Dataset**: Open
- **Reference**: [JailbreakBench: An Open Robustness Benchmark for Jailbreaking Large Language Models](https://arxiv.org/abs/2404.01318)
- **Summary**: Open robustness benchmark with evolving repository of adversarial prompts, standardized evaluation, and official leaderboard. NeurIPS 2024 Datasets and Benchmarks Track.

---

### [StrongREJECT](https://github.com/dsbowen/strong_reject)
- **Category**: Security4AI > Model Robustness > Jailbreak > Evaluation Metric
- **Created by**: UC Berkeley, Google DeepMind
- **Used by**: Academic community
- **Scale**: 313 forbidden prompts across 6 categories (illegal goods, non-violent crimes, hate/discrimination, disinformation, violence, sexual content)
- **Dataset**: Open
- **Reference**: [A StrongREJECT for Empty Jailbreaks](https://arxiv.org/abs/2402.10260)
- **Summary**: Jailbreak evaluation benchmark with rubric-based scoring that achieves state-of-the-art agreement with human judgments; shows many "successful" jailbreaks actually reduce model capabilities.

---

### [AdvBench](https://github.com/llm-attacks/llm-attacks)
- **Category**: Security4AI > Model Robustness > Adversarial Robustness > Harmful Behavior Dataset
- **Created by**: CMU, Google DeepMind
- **Used by**: Academic community (foundational dataset for GCG, PAIR, AutoDAN research)
- **Scale**: 520 harmful behaviors (harmful_behaviors.csv) + harmful strings dataset
- **Dataset**: Open
- **Reference**: [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/abs/2307.15043)
- **Summary**: Foundational harmful behavior dataset used as the standard evaluation set for adversarial attack research on LLMs (GCG, PAIR, AutoDAN, etc.).

---

### [GCG (Greedy Coordinate Gradient)](https://github.com/llm-attacks/llm-attacks)
- **Category**: Security4AI > Model Robustness > Adversarial Attack Method > Token-level
- **Created by**: CMU, Google DeepMind
- **Used by**: Academic community (baseline in JailbreakBench, HarmBench)
- **Scale**: Evaluated on AdvBench (520 behaviors); transferable to closed-source models (ChatGPT, Bard, Claude)
- **Dataset**: Open (attack code + AdvBench)
- **Reference**: [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/abs/2307.15043)
- **Summary**: Gradient-based adversarial suffix optimization that finds universal, transferable attack prompts across aligned LLMs. Foundational white-box attack method.

---

### [PAIR (Prompt Automatic Iterative Refinement)](https://github.com/patrickrchao/JailbreakingLLMs)
- **Category**: Security4AI > Model Robustness > Adversarial Attack Method > Black-box
- **Created by**: University of Pennsylvania
- **Used by**: Academic community (baseline in JailbreakBench)
- **Scale**: Black-box attack requiring <20 queries per jailbreak (250x more efficient than GCG)
- **Dataset**: Open
- **Reference**: [Jailbreaking Black Box Large Language Models in Twenty Queries](https://arxiv.org/abs/2310.08419)
- **Summary**: Black-box jailbreak method using an attacker LLM to iteratively refine prompts via in-context learning; achieves competitive success rates on GPT-3.5/4, Vicuna, PaLM-2.

---

### [AutoDAN](https://github.com/SheltonLiu-N/AutoDAN)
- **Category**: Security4AI > Model Robustness > Adversarial Attack Method > Genetic Algorithm
- **Created by**: University of Wisconsin-Madison
- **Used by**: Academic community (evaluated in EasyJailbreak, NeurIPS 2024 benchmarks)
- **Scale**: Generates semantically meaningful jailbreak prompts; evaluated on AdvBench
- **Dataset**: Open
- **Reference**: [AutoDAN: Generating Stealthy Jailbreak Prompts on Aligned Large Language Models](https://arxiv.org/abs/2310.04451)
- **Summary**: Hierarchical genetic algorithm that generates stealthy, semantically meaningful jailbreak prompts; bypasses perplexity-based defenses. ICLR 2024.

---

### [SafetyBench](https://github.com/thu-coai/SafetyBench)
- **Category**: Security4AI > Model Robustness > Safety > Comprehensive Evaluation
- **Created by**: Tsinghua University (CoAI Group)
- **Used by**: Academic community
- **Scale**: 11,435 multiple-choice questions across 7 safety categories, in English and Chinese
- **Dataset**: Open
- **Reference**: [SafetyBench: Evaluating the Safety of Large Language Models](https://arxiv.org/abs/2309.07045)
- **Summary**: Comprehensive bilingual (EN/ZH) safety benchmark evaluating 25+ LLMs on safety understanding; GPT-4 significantly outperforms others. ACL 2024.

---

### [SALAD-Bench](https://github.com/OpenSafetyLab/SALAD-BENCH)
- **Category**: Security4AI > Model Robustness > Safety > Attack/Defense Evaluation
- **Created by**: OpenSafetyLab (Peking University, others)
- **Used by**: Academic community
- **Scale**: 21,000 harmful base questions across 6 domains, 16 tasks, 66 categories; includes QA + multiple-choice variants
- **Dataset**: Open
- **Reference**: [SALAD-Bench: A Hierarchical and Comprehensive Safety Benchmark for Large Language Models](https://arxiv.org/abs/2402.05044)
- **Summary**: Large-scale hierarchical safety benchmark with polymorphic question types and built-in MD-Judge evaluator for both attack and defense evaluation. ACL 2024 Findings.

---

### [TrustLLM](https://github.com/HowieHwong/TrustLLM)
- **Category**: Security4AI > Model Robustness > Trustworthiness > Multi-dimensional
- **Created by**: UIUC, Stanford, UC Berkeley, CAIS, Microsoft Research
- **Used by**: Academic community
- **Scale**: 30+ datasets across 6 dimensions (truthfulness, safety, fairness, robustness, privacy, machine ethics); 16 LLMs evaluated
- **Dataset**: Open
- **Reference**: [TrustLLM: Trustworthiness in Large Language Models](https://arxiv.org/abs/2401.05561)
- **Summary**: Multi-dimensional trustworthiness framework finding positive correlation between capability and trustworthiness; proprietary LLMs generally outperform open-source. ICML 2024.

---

### [DecodingTrust](https://github.com/AI-secure/DecodingTrust)
- **Category**: Security4AI > Model Robustness > Trustworthiness > GPT Assessment
- **Created by**: UIUC, Stanford, UC Berkeley, CAIS, Microsoft Research
- **Used by**: Academic community
- **Scale**: 8 trustworthiness dimensions (toxicity, stereotype bias, adversarial robustness, OOD robustness, privacy, machine ethics, fairness, adversarial demonstrations)
- **Dataset**: Open
- **Reference**: [DecodingTrust: A Comprehensive Assessment of Trustworthiness in GPT Models](https://arxiv.org/abs/2306.11698)
- **Summary**: Comprehensive GPT trustworthiness assessment; found GPT-4 more vulnerable to jailbreaking than GPT-3.5 despite higher baseline trustworthiness. NeurIPS 2023 Outstanding Paper (Benchmarks Track) + NSA Best Cybersecurity Paper 2024.

---

### [AgentDojo](https://github.com/ethz-spylab/agentdojo)
- **Category**: Security4AI > Model Robustness > Prompt Injection > Agentic
- **Created by**: ETH Zurich
- **Used by**: xAI (in official evals)
- **Scale**: 97 realistic tasks, 629 security test cases across email, banking, travel scenarios
- **Dataset**: Open
- **Reference**: [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352)
- **Summary**: Dynamic evaluation framework for prompt injection attacks on tool-using LLM agents; state-of-the-art LLMs solve <66% of tasks even without attacks. NeurIPS 2024 Datasets and Benchmarks Track.

---

### [CyberSecEval (Purple Llama)](https://github.com/meta-llama/PurpleLlama)
- **Category**: Security4AI > Model Robustness > Secure Code Generation + Cyberattack Compliance
- **Created by**: Meta AI
- **Used by**: Meta (Llama evaluations), academic community
- **Scale**: ~1,000 test cases; 189 static analysis rules covering 50 CWEs (v1); 500 interpreter abuse prompts (v2); prompt injection + social engineering + autonomous cyber ops (v3); CyberSOCEval + AutoPatchBench (v4)
- **Dataset**: Open
- **Reference (v1)**: [Purple Llama CyberSecEval: A Secure Coding Benchmark for Language Models](https://arxiv.org/abs/2312.04724)
- **Reference (v2)**: [CyberSecEval 2: A Wide-Ranging Cybersecurity Evaluation Suite for Large Language Models](https://arxiv.org/abs/2404.13161)
- **Reference (v3)**: [CyberSecEval 3: Advancing the Evaluation of Cybersecurity Risks and Capabilities in Large Language Models](https://arxiv.org/abs/2408.01605)
- **Summary**: Meta's comprehensive, evolving LLM cybersecurity evaluation suite spanning insecure code generation, cyberattack compliance, prompt injection, interpreter abuse, exploit generation, social engineering, and SOC automation. Open-sourced as part of Purple Llama.

---

### [CodeShield (Purple Llama)](https://github.com/meta-llama/PurpleLlama/tree/main/CodeShield)
- **Category**: Security4AI > Model Robustness > Secure Code Filtering > Inference-time
- **Created by**: Meta AI
- **Used by**: Meta (Llama deployments)
- **Scale**: Two-layer scanning solution (pattern detection + deep analysis)
- **Dataset**: Open (tool, not dataset)
- **Summary**: Inference-time insecure code filtering tool that prevents LLM-generated insecure code from reaching production. Part of the Purple Llama safety suite.
