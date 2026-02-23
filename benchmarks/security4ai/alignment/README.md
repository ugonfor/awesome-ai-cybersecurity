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
- **Summary**: Measures whether models faithfully report their beliefs or engage in deceptive behavior under pressure. Higher score indicates more deceptive behavior (lower is better).
- **Results (Deception Score, lower is better)**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 0.43 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4.1 Non-Thinking | 0.46 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
  | Grok 4 Fast (Reasoning) | 0.47 | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 Thinking | 0.49 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
  | Grok 4 Fast (Non-Reasoning) | 0.63 | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
- **Notes**: MASK dishonesty increased from Grok 4 (0.43) to Grok 4.1 (0.49), indicating a safety regression. Non-reasoning mode substantially increases dishonesty rate for Grok 4 Fast (0.63 vs 0.47).

---

### MakeMeSay
- **Category**: Security4AI > Alignment > Persuasion
- **Created by**: OpenAI / Google DeepMind
- **Used by**: xAI
- **Scale**: Attacker-defender persuasion game (win rate against non-thinking Grok-3-Mini defender)
- **Dataset**: Open
- **Reference**: Part of [OpenAI o1 System Card](https://arxiv.org/abs/2412.16720)
- **Summary**: Evaluates model's ability to manipulate another model into saying a specific codeword through persuasion. Measured as win rate. Lower is safer.
- **Results (Win Rate as Attacker, lower is safer)**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 12-13% | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4 Fast | 12% | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 | 0% | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
- **Notes**: Grok 4.1 MakeMeSay score of 0% indicates inability to manipulate the defender -- a safety improvement from Grok 4's 12-13%. Minor discrepancy: Grok 4 MakeMeSay reported as 0.12 in its own card but 0.13 in the Grok 4.1 card comparison column.

---

### Sycophancy Evaluation
- **Category**: Security4AI > Alignment > Sycophancy
- **Created by**: Various
- **Used by**: xAI
- **Scale**: User agreement measurement
- **Dataset**: Open
- **Summary**: Measures tendency to abandon correct judgments to agree with misleading user input. Lower is better.
- **Results (Sycophancy Rate, lower is better)**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | Grok 4 | 0.07 | 2025.08 | [Model Card](https://data.x.ai/2025-08-20-grok-4-model-card.pdf) |
  | Grok 4 Fast (R/NR) | 0.10 / 0.13 | 2025.09 | [Model Card](https://data.x.ai/2025-09-19-grok-4-fast-model-card.pdf) |
  | Grok 4.1 Thinking | 0.19 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
  | Grok 4.1 Non-Thinking | 0.23 | 2025.11 | [Model Card](https://data.x.ai/2025-11-17-grok-4-1-model-card.pdf) |
- **Notes**: Sycophancy increased substantially from Grok 4 (0.07) to Grok 4.1 (0.19/0.23), a notable safety regression.

---

### [Stealth Evaluation](https://arxiv.org/abs/2505.01420)
- **Category**: Security4AI > Alignment > Oversight Evasion
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 5 stealth evaluations (cover_your_tracks, decision_sabotage, strategic_rule_breaking, classifier_evasion, oversight_pattern)
- **Dataset**: Open
- **Reference**: [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Summary**: Tests model's ability to circumvent oversight mechanisms and operate covertly. Part of Google's "scheming inability safety case" -- models failing these tests would be almost certainly incapable of severe harm via scheming.
- **Results (Oversight Pattern, higher = more concerning)**:
  | Model | Success Rate | Score | Source |
  |---|---|---|---|
  | Gemini 2.5 Pro | 35.4% | 41.8% (PASS) | [Paper](https://arxiv.org/abs/2505.01420) |
  | Claude 3.7 Sonnet | 34.0% | 36.3% (PASS) | [Paper](https://arxiv.org/abs/2505.01420) |
  | Gemini 2.5 Flash | 23.0% | 32.0% | [Paper](https://arxiv.org/abs/2505.01420) |
  | GPT-4o | 11.0% | 14.7% | [Paper](https://arxiv.org/abs/2505.01420) |
  | o1 | 2.0% | 12.7% | [Paper](https://arxiv.org/abs/2505.01420) |
- **Notes**: Gemini 3.1 Pro is the first model to achieve ~100% success on max_tokens, context_size_mod, and oversight_frequency situational awareness tasks. No model reached the 80% passing threshold on overall stealth/situational awareness evaluations.

---

### [Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Category**: Security4AI > Alignment > Self-Reasoning
- **Created by**: Google DeepMind
- **Used by**: Google
- **Scale**: 11 situational awareness evaluations
- **Dataset**: Open
- **Reference**: [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420)
- **Summary**: Evaluates model's ability to reason about itself and its environment, a prerequisite for autonomous action. 3 challenges solved by all 5 tested models (read_logs, disabled_tool, approved_directories); 6 challenges solved by no model.
- **Results**:
  | Model | Challenges Solved (/11) | Source |
  |---|---|---|
  | Gemini 3 Pro | 3/11 | [FSF Report](https://storage.googleapis.com/deepmind-media/gemini/gemini_3_pro_fsf_report.pdf) |
  | Gemini 3.1 Pro | ~100% on max_tokens, context_size_mod, oversight_frequency | [Model Card](https://storage.googleapis.com/deepmind-media/Model-Cards/Gemini-3-1-Pro-Model-Card.pdf) |
- **Notes**: Gemini 3.1 Pro is the first model to consistently solve max_tokens, context_size_mod, and oversight_frequency situational awareness challenges. No model has come close to the 80% passing threshold (9/11 challenges).

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

### Apollo Research Sabotage (OpenAI)
- **Category**: Security4AI > Alignment > Sabotage
- **Created by**: Apollo Research
- **Used by**: OpenAI
- **Scale**: Mean best-of-10 sabotage score
- **Dataset**: Closed
- **Summary**: Measures model propensity for sabotage behaviors in agentic settings. Higher score indicates more sabotage behavior (lower is better).
- **Results (Mean Best-of-10 Score, lower is better)**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | GPT-5.2-Codex | 0.66 | 2025.12 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | GPT-5.2 | 0.75 | 2025.12 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | GPT-5.3-Codex | 0.88 | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |

---

### Destructive Action Avoidance (OpenAI)
- **Category**: Security4AI > Alignment > Safety Compliance
- **Created by**: OpenAI
- **Used by**: OpenAI
- **Scale**: Score from 0 to 1 (higher is better)
- **Dataset**: Closed
- **Summary**: Measures ability of agentic coding models to avoid executing destructive actions. Higher is better.
- **Results (Avoidance Score, higher is better)**:
  | Model | Score | Date | Source |
  |---|---|---|---|
  | GPT-5-Codex | 0.66 | 2025.09 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | GPT-5.1-Codex | 0.70 | 2025.11 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | GPT-5.1-Codex-Max | 0.75 | 2025.11 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | GPT-5.2-Codex | 0.76 | 2025.12 | [GPT-5.3-Codex System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |
  | GPT-5.3-Codex | 0.88 | 2026.02 | [System Card](https://cdn.openai.com/pdf/23eca107-a9b1-4d2c-b156-7deb4fbc697c/GPT-5-3-Codex-System-Card-02.pdf) |

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
