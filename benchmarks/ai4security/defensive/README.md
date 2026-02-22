# AI4Security — Defensive Capability Benchmarks

> AI performing defensive cybersecurity tasks: detection, investigation, SOC automation, threat intelligence.

---

*Note: Most current vendor evaluations focus on offensive capabilities (CTF, exploit, pentest). Defensive benchmarks are emerging but underrepresented in vendor documentation. See the academic benchmarks section for community-driven defensive evaluation efforts.*

### Cybersecurity Investigation Benchmark (Anthropic)
- **Category**: AI4Security > Defensive Capability > Investigation
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: 40 cybersecurity investigations
- **Dataset**: Closed
- **Summary**: Blind-ranked comparison of AI models on realistic cybersecurity investigation tasks.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Claude Opus 4.6 | Best in 38/40 blind-ranked comparisons | 2026.02 | [System Card](https://anthropic.com/claude-opus-4-6-system-card) |

---

## Academic Benchmarks (Community-Driven)

> The following defensive benchmarks originate from the academic community.

---

### [CyberSOCEval (CyberSecEval 4)](https://meta-llama.github.io/PurpleLlama/CyberSecEval/)
- **Category**: AI4Security > Defensive Capability > SOC Automation
- **Created by**: Meta AI (in collaboration with CrowdStrike)
- **Used by**: Meta (Llama evaluations)
- **Scale**: Two benchmarks: Malware Analysis + Threat Intelligence Reasoning
- **Dataset**: Open
- **Summary**: Evaluates LLM capabilities for Security Operation Center efficiency improvements including malware analysis and threat intelligence reasoning. Part of CyberSecEval 4, developed with CrowdStrike.

---

### [AutoPatchBench (CyberSecEval 4)](https://meta-llama.github.io/PurpleLlama/CyberSecEval/)
- **Category**: AI4Security > Defensive Capability > Vulnerability Patching
- **Created by**: Meta AI
- **Used by**: Meta (Llama evaluations)
- **Scale**: Automated security patch generation for native code vulnerabilities
- **Dataset**: Open
- **Summary**: Measures LLM agent's capability to automatically patch security vulnerabilities in native code. Part of CyberSecEval 4.
