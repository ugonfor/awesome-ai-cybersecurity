# Evaluation Tools & Frameworks

> Frameworks, platforms, and tools for running cybersecurity AI benchmarks and evaluations.

---

## Evaluation Frameworks

### [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)
- **Category**: Evaluation Framework
- **Created by**: UK AI Safety Institute
- **Open Source**: Yes (Apache 2.0)
- **Summary**: Open-source Python framework for building and running reproducible LLM evaluations with multi-turn dialog, tool usage, and sandboxed execution.

### [Inspect Cyber](https://inspect.cyber.aisi.org.uk/)
- **Category**: Evaluation Framework > Cybersecurity
- **Created by**: UK AI Safety Institute
- **Open Source**: Yes
- **Summary**: Specialized extension of Inspect AI for creating agentic cyber evaluations with YAML configs, converting them into sandboxed CTF and cyber range environments.
- **Reference**: [Blog](https://www.aisi.gov.uk/blog/inspect-cyber)

### [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals)
- **Category**: Evaluation Framework > Task Collection
- **Created by**: UK AISI, Arcadia Impact, Vector Institute
- **Open Source**: Yes
- **Summary**: Community-contributed LLM benchmark evaluations including Cybench, CVEBench, WMDP-Cyber, CyberMetric, SEvenLLM, AgentHarm, and AgentDojo.

### [Vivaria](https://github.com/METR/vivaria)
- **Category**: Evaluation Framework
- **Created by**: METR (Model Evaluation and Threat Research)
- **Open Source**: Yes
- **Summary**: Web application for running AI agent evaluations using the METR Task Standard with sandboxed task environments. Transitioning to Inspect AI.

### [Google DeepMind Dangerous Capability Evaluations](https://github.com/google-deepmind/dangerous-capability-evaluations)
- **Category**: Evaluation Framework
- **Created by**: Google DeepMind
- **Open Source**: Partial (13 in-house CTF challenges open-sourced)
- **Summary**: Framework for evaluating frontier AI models for dangerous capabilities across cybersecurity, biosecurity, and autonomy with CCL thresholds.
- **Reference**: [Evaluating Frontier Models for Dangerous Capabilities](https://arxiv.org/abs/2403.13793)

### [EleutherAI lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness)
- **Category**: Evaluation Framework
- **Created by**: EleutherAI
- **Open Source**: Yes
- **Summary**: Unified framework for few-shot LLM evaluation on hundreds of tasks including WMDP-Cyber. Backend for HuggingFace Open LLM Leaderboard.

---

## Benchmark Suites

### [PurpleLlama / CyberSecEval](https://github.com/meta-llama/PurpleLlama)
- **Category**: Benchmark Suite
- **Created by**: Meta
- **Open Source**: Yes
- **Summary**: Comprehensive suite evaluating LLM cybersecurity risks: insecure code generation, cyberattack compliance, false refusals, SOC capabilities (CyberSOCEval w/ CrowdStrike), and auto-patching.
- **Reference**: [Purple Llama CyberSecEval](https://arxiv.org/abs/2312.04724)

### [CAIBench](https://arxiv.org/abs/2510.24317)
- **Category**: Benchmark Suite > Meta-Benchmark
- **Created by**: Alias Robotics
- **Open Source**: Yes
- **Summary**: Modular meta-benchmark integrating 5 evaluation categories (CTF, attack/defense, cyber range, knowledge, privacy) covering 10,000+ instances.
- **Reference**: [Cybersecurity AI Benchmark (CAIBench)](https://arxiv.org/abs/2510.24317)

### [ExCyTIn-Bench](https://github.com/microsoft/SecRL)
- **Category**: Benchmark Suite > Threat Investigation
- **Created by**: Microsoft
- **Open Source**: Yes
- **Summary**: Evaluates AI agents on real-world cyber threat investigation in simulated SOC environments using 57 log tables from Microsoft Sentinel with 589 Q&A pairs.
- **Reference**: [ExCyTIn-Bench](https://arxiv.org/abs/2507.14201)

### [eyeballvul](https://github.com/timothee-chauvin/eyeballvul)
- **Category**: Benchmark Suite > Vulnerability Detection
- **Created by**: Timothee Chauvin (METR-affiliated)
- **Open Source**: Yes
- **Summary**: Future-proof vulnerability detection benchmark with 24,000+ real vulnerabilities across 6,000+ revisions, updated weekly from published CVEs.
- **Reference**: [eyeballvul: a future-proof benchmark](https://arxiv.org/abs/2407.08708)

---

## Red Team / Adversarial Testing Tools

### [HarmBench](https://github.com/centerforaisafety/HarmBench)
- **Category**: Red Team Tool
- **Created by**: Center for AI Safety (CAIS)
- **Open Source**: Yes
- **Summary**: Standardized evaluation framework comparing 18 attack methods against 33 target LLMs/defenses with robust refusal metrics.
- **Reference**: [HarmBench: A Standardized Evaluation Framework](https://arxiv.org/abs/2402.04249)

### [StrongREJECT](https://github.com/dsbowen/strong_reject)
- **Category**: Red Team Tool > Jailbreak Evaluation
- **Created by**: UC Berkeley / Google DeepMind
- **Open Source**: Yes
- **Summary**: Jailbreak evaluation benchmark with 313 forbidden prompts and automated evaluator achieving SOTA agreement with human judgments.
- **Reference**: [A StrongREJECT for Empty Jailbreaks](https://arxiv.org/abs/2402.10260)

### [JailbreakBench](https://github.com/JailbreakBench/jailbreakbench)
- **Category**: Red Team Tool > Jailbreak Leaderboard
- **Created by**: Multi-institutional academic collaboration
- **Open Source**: Yes
- **Summary**: Open robustness benchmark with 100 misuse behaviors, standardized threat model, jailbreak artifact repository, and attack/defense leaderboard.
- **Reference**: [JailbreakBench](https://arxiv.org/abs/2404.01318)

### [Garak](https://github.com/NVIDIA/garak)
- **Category**: Red Team Tool > Vulnerability Scanner
- **Created by**: NVIDIA
- **Open Source**: Yes
- **Summary**: LLM vulnerability scanner with dozens of probe plugins covering prompt injection, jailbreaking, data leakage, toxicity, and hallucination.

### [Promptfoo](https://github.com/promptfoo/promptfoo)
- **Category**: Red Team Tool > LLM Pentesting
- **Created by**: Promptfoo (open-source project)
- **Open Source**: Yes
- **Summary**: CLI tool for LLM red teaming and vulnerability scanning with OWASP LLM Top 10 presets and CI/CD integration.

---

## CTF Platforms

### [CTFd](https://github.com/CTFd/CTFd)
- **Category**: CTF Platform
- **Created by**: CTFd LLC
- **Open Source**: Yes (Apache 2.0)
- **Summary**: Most widely used open-source CTF framework for hosting competitions with dynamic scoring and challenge plugins. Many AI benchmarks use CTFd-style formats.

### [picoCTF](https://picoctf.org/)
- **Category**: CTF Platform
- **Created by**: Carnegie Mellon University (CyLab)
- **Open Source**: Challenges open after competitions
- **Summary**: Year-round cybersecurity learning platform with 800,000+ active users. Claude ranked top 3% in picoCTF 2025.

### [Hack The Box](https://www.hackthebox.com/)
- **Category**: CTF Platform / AI Cyber Range
- **Created by**: Hack The Box
- **Open Source**: No (commercial)
- **Summary**: Professional cybersecurity training platform. Launched HTB AI Range (Dec 2025) for benchmarking autonomous AI security agents.

---

## Simulation Environments

### [CyberBattleSim](https://github.com/microsoft/CyberBattleSim)
- **Category**: Simulation > Network Attack/Defense
- **Created by**: Microsoft Research
- **Open Source**: Yes (MIT)
- **Summary**: OpenAI Gym environment where RL-trained attacker agents spread through abstract enterprise networks while defender agents mitigate.

### [ControlArena](https://control-arena.aisi.org.uk/)
- **Category**: Simulation > AI Control
- **Created by**: UK AISI + Redwood Research
- **Open Source**: Yes
- **Summary**: Library for running AI control experiments on Inspect AI, evaluating protocols designed to prevent unsafe actions by misaligned AI systems.
