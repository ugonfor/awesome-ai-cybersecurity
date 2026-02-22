# Security4AI — Alignment Benchmarks

> Ensuring AI behaves as intended: deception measurement, persuasion resistance, oversight compliance, sabotage prevention.

---

### [MASK](https://arxiv.org/abs/2503.03750)
- **Category**: Security4AI > Alignment > Deception
- **Created by**: Center for AI Safety (CAIS)
- **Used by**: xAI
- **Scale**: Multi-scenario deception measurement
- **Dataset**: Open ([GitHub](https://github.com/centerforaisafety/mask))
- **Reference**: [The MASK Benchmark: Disentangling Honesty From Accuracy in AI Systems](https://arxiv.org/abs/2503.03750)
- **Summary**: Measures whether models faithfully report their beliefs or engage in deceptive behavior under pressure.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 0.43 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4.1 Thinking | 0.49 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### MakeMeSay
- **Category**: Security4AI > Alignment > Persuasion
- **Created by**: OpenAI (adapted from Google DeepMind methodology)
- **Used by**: xAI
- **Scale**: Attacker-defender persuasion game
- **Dataset**: Open
- **Summary**: Evaluates model's ability to manipulate another model into saying a specific codeword through persuasion.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4.1 | 0% (as attacker) | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### Sycophancy Evaluation
- **Category**: Security4AI > Alignment > Sycophancy
- **Created by**: Various
- **Used by**: xAI
- **Scale**: User agreement measurement
- **Dataset**: Open
- **Summary**: Measures tendency to abandon correct judgments to agree with misleading user input.
- **Results**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 0.07 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4.1 Thinking | 0.19 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |

---

### [Stealth Evaluation](https://arxiv.org/abs/2505.01420)
- **Category**: Security4AI > Alignment > Oversight Evasion
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 5 stealth evaluations
- **Dataset**: Open
- **Reference**: [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Summary**: Tests model's ability to circumvent oversight mechanisms and operate covertly.

---

### [Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Category**: Security4AI > Alignment > Self-Reasoning
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 11 situational awareness evaluations
- **Dataset**: Open
- **Reference**: [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Summary**: Evaluates model's ability to reason about itself and its environment, a prerequisite for autonomous action.

---

### [Sabotage Risk Assessment](https://alignment.anthropic.com/2025/sabotage-risk-report/)
- **Category**: Security4AI > Alignment > Sabotage
- **Created by**: Anthropic
- **Used by**: Anthropic
- **Scale**: 9 sabotage pathways
- **Dataset**: Closed
- **Reference**: [Pilot Sabotage Risk Report](https://alignment.anthropic.com/2025/sabotage-risk-report/2025_pilot_risk_report.pdf)
- **Summary**: Evaluates 9 pathways through which AI models could deliberately sabotage their operators. Reviewed by METR.

---

## Academic Benchmarks (Community-Driven)

---

### [WMDP (Weapons of Mass Destruction Proxy)](https://github.com/centerforaisafety/wmdp)
- **Category**: Security4AI > Alignment > Hazardous Knowledge
- **Created by**: Center for AI Safety (CAIS), Scale AI, 20+ academic institutions
- **Used by**: xAI (WMDP-Cyber subset)
- **Scale**: 3,668 multiple-choice questions across biosecurity, cybersecurity, and chemical security
- **Dataset**: Open (filtered to remove sensitive info)
- **Reference**: [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/abs/2403.03218)
- **Summary**: Measures hazardous knowledge that could enable malicious use in bio/cyber/chem domains; also benchmarks unlearning methods (RMU) for removing hazardous knowledge while retaining general capabilities. ICML 2024.
- **Cross-reference**: Also listed under [AI4Security > Cyber Knowledge](../../ai4security/knowledge/README.md) as a knowledge benchmark.
