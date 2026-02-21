# Anthropic: System Cards, Model Cards, and Technical Reports

## Cybersecurity Evaluation Framework

Anthropic evaluates cybersecurity under the **Responsible Scaling Policy (RSP)** with **AI Safety Levels (ASL)**. Cybersecurity is one of three catastrophic risk domains (alongside CBRN and autonomous capabilities).

**ASL-3 Cyber Threshold**: Model achieves success ≥1/5 times in ≥2/6 classes of expert vulnerability discovery and exploit development evaluations.

### Primary Benchmarks

| Benchmark | Description |
|---|---|
| **Cybench** | 40 professional-level CTF tasks from 4 competitions |
| **CyberGym** | Vulnerability detection in real open-source software (1,507 known CVEs) |
| **CMU Cyber Ranges** | ~50-host network simulations for end-to-end attack chains |
| **Custom Network Challenges** | Anthropic-built network infiltration scenarios |
| **Real CTF Competitions** | PicoCTF, HackTheBox, WRCCDC |

---

## Documents

### 1. Claude 2 Model Card

- **Date**: July 2023
- **URL**: https://www.anthropic.com/claude-2-model-card | [PDF](https://www-cdn.anthropic.com/bd2a28d2535bfb0494cc8e2a3bf135d2e7523226/Model-Card-Claude-2.pdf)
- **Models**: Claude 1.3, Claude 2
- **Benchmarks**: Red-teaming (crowd-worker), national security risk eval, ARC safety audit, harmful response testing (328 prompts)
- **Note**: No dedicated cybersecurity benchmarks (CTF etc.) at this stage

### 2. Responsible Scaling Policy (RSP) v1.0

- **Date**: September 19, 2023
- **URL**: https://www.anthropic.com/rsp-updates | [PDF](https://www-cdn.anthropic.com/1adf000c8f675958c2ee23805d91aaade1cd4613/responsible-scaling-policy.pdf)
- **Models**: Framework for all Claude models
- **Content**: Establishes ASL framework, defines cybersecurity as catastrophic risk domain, sets ASL-3 threshold

### 3. Frontier Threats Red Teaming for AI Safety

- **Date**: July 2023
- **URL**: https://www.anthropic.com/news/frontier-threats-red-teaming-for-ai-safety
- **Models**: Pre-Claude 2 snapshots, Claude 2
- **Content**: Biosecurity-focused but establishes methodology for dual-use capability assessment

### 4. Claude 3 Model Card (Opus, Sonnet, Haiku)

- **Date**: March 2024
- **URL**: https://www-cdn.anthropic.com/c6a80a657af445f40e31afac050f3bf76d3b1404.pdf
- **Models**: Claude 3 Haiku, Sonnet, Opus
- **Benchmarks**: CTF challenges (pwn, RE, crypto, web)
- **Classification**: ASL-2

### 5. Claude 3.5 Sonnet Model Card Addendum

- **Date**: June 2024
- **URL**: https://www-cdn.anthropic.com/fed9cc193a14b84131812372d8d5857f8f304c52/Model_Card_Claude_3_Addendum.pdf
- **Models**: Claude 3.5 Sonnet (original)
- **Benchmarks**: CTF (pwn, RE, crypto, web)
- **Classification**: ASL-2
- **Note**: US/UK AISI later used **Cybench** for Joint Pre-Deployment Test

### 6. Claude 3.5 Haiku / Upgraded 3.5 Sonnet Addendum

- **Date**: October 2024
- **URL**: https://www-cdn.anthropic.com/c7822cdc35ad788ec87e14b3a9d45010f1f86c38.pdf
- **Models**: Claude 3.5 Haiku, Claude 3.5 Sonnet (upgraded)
- **Benchmarks**: CTF-based evaluations
- **Classification**: ASL-2

### 7. Claude 3.7 Sonnet System Card

- **Date**: February 2025
- **URL**: https://anthropic.com/claude-3-7-sonnet-system-card | [PDF](https://www-cdn.anthropic.com/9ff93dfa8f445c932415d335c88852ef47f1201e.pdf)
- **Models**: Claude 3.7 Sonnet
- **Benchmarks**: **Cybench** 35.9% success rate, prompt injection evals
- **Classification**: ASL-2

### 8. RSP v2.2

- **Date**: May 14, 2025
- **URL**: https://www.anthropic.com/responsible-scaling-policy
- **Models**: Framework for all models (triggered for Claude Opus 4)
- **Content**: Updated capability thresholds, ASL-3 Security/Deployment Standards

### 9. Claude Opus 4 & Sonnet 4 System Card

- **Date**: May 2025
- **URL**: https://www.anthropic.com/claude-4-system-card | [PDF](https://www-cdn.anthropic.com/07b2a3f9902ee19fe39a36ca638e5ae987bc64dd.pdf)
- **Models**: Claude Opus 4, Claude Sonnet 4
- **Benchmarks**: Cybench, custom network challenges, cyber-harness network challenges
  - Opus: 11/11 easy, 1/2 medium, 0/2 hard
  - Sonnet: 10/11 easy, 1/2 medium, 0/2 hard
- **Classification**: **First ASL-3** (Opus 4)
- **Note**: ~120-page system card

### 10. ASL-3 Deployment Safeguards Report

- **Date**: May 2025
- **URL**: https://www.anthropic.com/asl3-deployment-safeguards
- **Models**: Claude Opus 4
- **Content**: Threat modeling, defense-in-depth, universal jailbreak resistance, access controls

### 11. Activating ASL-3 Protections Report

- **Date**: May 2025
- **URL**: https://www.anthropic.com/activating-asl3-report
- **Models**: Claude Opus 4
- **Content**: Evidence of exceeding ASL-3 thresholds in cyber and CBRN

### 12. Cyber Competitions (Frontier Red Team)

- **Date**: 2025
- **URL**: https://red.anthropic.com/2025/cyber-competitions/
- **Models**: Claude
- **Benchmarks**:
  - PicoCTF 2025: 297th/10,460 teams (top 3%), 32/41 challenges
  - HackTheBox AI vs Human: 30th/161 overall, 4th/8 AI teams, 19/20 challenges
  - WRCCDC Regional: 6th/9 teams
  - WRCCDC Qualifier: 10th/28 teams
  - PlaidCTF: 0 challenges solved (advanced difficulty)
  - DEF CON CTF Qualifier: 0 challenges solved
  - Airbnb Competition: 15/30 challenges, 39th/~180 teams

### 13. AI for Cyber Defenders (Frontier Red Team)

- **Date**: 2025
- **URL**: https://red.anthropic.com/2025/ai-for-cyber-defenders/
- **Models**: Claude Sonnet 4, Claude Sonnet 4.5
- **Benchmarks**: **CyberGym**
  - Sonnet 4: strongest on public leaderboard
  - Sonnet 4.5: SOTA 28.9% ($2 cost), 66.7% vuln reproduction (30 trials), 33%+ new vuln discovery (30 trials)

### 14. Progress from Frontier Red Team

- **Date**: 2025
- **URL**: https://www.anthropic.com/news/strategic-warning-for-ai-risk-progress-and-insights-from-our-frontier-red-team
- **Models**: Multiple Claude models (longitudinal)
- **Content**: Models approaching undergraduate-level cybersecurity skills

### 15. Framework for Evaluating Emerging Cyberattack Capabilities

- **Date**: March 14, 2025
- **URL**: https://arxiv.org/abs/2503.11917
- **Models**: Frontier AI models including Claude
- **Content**: End-to-end attack chain framework, 12,000+ real-world AI-in-cyber incidents, 50 new challenges

### 16. Claude Opus 4.1 System Card Addendum

- **Date**: August 2025
- **URL**: https://www.anthropic.com/claude-opus-4-1-system-card | [PDF](https://www-cdn.anthropic.com/9fa30625273bafdf5af82c93719d7ca606485a16.pdf)
- **Models**: Claude Opus 4.1
- **Benchmarks**: Cybench, custom cyber challenges
- **Classification**: ASL-3 maintained

### 17. Pilot Sabotage Risk Report

- **Date**: Summer 2025
- **URL**: https://alignment.anthropic.com/2025/sabotage-risk-report/ | [PDF](https://alignment.anthropic.com/2025/sabotage-risk-report/2025_pilot_risk_report.pdf)
- **Models**: Claude Opus 4
- **Content**: 9 sabotage risk pathways, reviewed by METR

### 18. Threat Intelligence Report: AI-Orchestrated Cyber Espionage

- **Date**: August/September 2025
- **URL**: https://www.anthropic.com/news/disrupting-AI-espionage | [PDF](https://assets.anthropic.com/m/ec212e6566a0d47/original/Disrupting-the-first-reported-AI-orchestrated-cyber-espionage-campaign.pdf)
- **Models**: Claude (adversary use in the wild)
- **Content**: First documented AI-orchestrated cyber espionage (Chinese state-sponsored GTG-1002), data extortion via Claude Code (17+ orgs), North Korean schemes

### 19. Claude Sonnet 4.5 System Card

- **Date**: September 2025
- **URL**: https://www.anthropic.com/claude-sonnet-4-5-system-card | [PDF](https://www-cdn.anthropic.com/963373e433e489a87a10c823c52a0a013e9172dd.pdf)
- **Models**: Claude Sonnet 4.5
- **Benchmarks**:
  - Cybench: **76.5%** (doubled from 3.7 Sonnet's 35.9%)
  - CyberGym: SOTA 28.9%
  - CMU cyber ranges: ~50-host networks
  - Equifax simulation: 2/5 trials autonomous success

### 20. Claude Haiku 4.5 System Card

- **Date**: October 2025
- **URL**: https://www.anthropic.com/claude-haiku-4-5-system-card | [PDF](https://www-cdn.anthropic.com/7aad69bf12627d42234e01ee7c36305dc2f6a970.pdf)
- **Models**: Claude Haiku 4.5
- **Classification**: ASL-2
- **Benchmarks**: RSP evaluations, 87.7% appropriate assistance on legitimate security research

### 21. Claude Opus 4.5 System Card

- **Date**: November 2025
- **URL**: https://www.anthropic.com/claude-opus-4-5-system-card | [PDF](https://www-cdn.anthropic.com/bf10f64990cfda0ba858290be7b8cc6317685f47.pdf)
- **Models**: Claude Opus 4.5
- **Benchmarks**: Cybench, network challenges, cyber-harness network challenges
- **Notable**: First successful network challenge solve without human assistance

### 22. AI Models on Realistic Cyber Ranges (Frontier Red Team)

- **Date**: January 16, 2026
- **URL**: https://red.anthropic.com/2026/cyber-toolkits-update/
- **Models**: Claude Sonnet 4.5
- **Benchmarks**: Equifax cyber range (2/5 autonomous), 9 network simulations, instant CVE recognition

### 23. Claude Opus 4.6 System Card

- **Date**: February 2026
- **URL**: https://anthropic.com/claude-opus-4-6-system-card | [PDF](https://www-cdn.anthropic.com/0dd865075ad3132672ee0ab40b05a53f14cf5288.pdf)
- **Models**: Claude Opus 4.6
- **Benchmarks**:
  - Cybench CTF
  - CyberGym (1,507 known CVEs)
  - 40 cybersecurity investigations: best in 38/40 blind-ranked comparisons
  - 500+ zero-day vulnerabilities discovered in pre-release testing
  - 6 new cybersecurity probes
- **Note**: 213-page system card

### 24. Claude Sonnet 4.6 System Card

- **Date**: February 17, 2026
- **URL**: https://anthropic.com/claude-sonnet-4-6-system-card
- **Models**: Claude Sonnet 4.6
- **Benchmarks**: Prompt injection resistance (0% in coding w/ extended thinking, <0.3% in browser)

---

## Cybench Performance Progression

| Model | Date | Cybench Score |
|---|---|---|
| Claude 3.7 Sonnet | 2025.02 | 35.9% |
| Claude Sonnet 4.5 | 2025.09 | 76.5% |
| Claude Opus 4.6 | 2026.02 | SOTA (38/40 blind comparisons) |

## Key Milestones

- **First ASL-3**: Claude Opus 4 (May 2025)
- **First real-world adversary use documented**: August 2025 (Chinese state-sponsored)
- **First 500+ zero-day discovery**: Claude Opus 4.6 (February 2026)
