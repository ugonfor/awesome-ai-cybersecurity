# CLAUDE.md

## Project Overview

**awesome-ai-cybersecurity** — A curated list of AI cybersecurity benchmarks, agents, and tools, organized by a clear taxonomy.

- GitHub: https://github.com/ugonfor/awesome-ai-cybersecurity
- Scope: Benchmarks, Agents/Tools (NO papers-only entries — papers are linked as references within entries)
- Target companies/models: OpenAI, Anthropic (Claude), Google (Gemini), xAI (Grok) and beyond

## How to Behave

### Taxonomy Rules (MUST follow)

Everything in this repo is classified by two levels. **Never create content that violates this structure.**

**Level 1 — AI4Security / Security4AI:**
- **AI4Security** = AI helping with cybersecurity tasks (CTF, pentest, SOC, threat intel, knowledge)
- **Security4AI** = Security concerns about AI itself (robustness, misuse, alignment)

**Level 2 — Subcategories:**

AI4Security:
- **Offensive Capability** = CTF, exploitation, penetration testing, vulnerability discovery, end-to-end attacks
- **Defensive Capability** = Detection, investigation, SOC automation, threat intelligence analysis
- **Cyber Knowledge** = Domain knowledge evaluation (WMDP-Cyber, CTI-MCQ, SecBench)

Security4AI:
- **Model Robustness** = Protecting models from attacks (prompt injection, jailbreak, adversarial robustness)
- **Misuse Risk** = Preventing harmful use of AI (AgentHarm, harmful refusal, malware generation)
- **Alignment** = Ensuring AI behaves as intended (sabotage, deception, sycophancy, stealth)

When adding new entries:
- ALL agents go under **AI4Security** (they perform cybersecurity tasks). Use subcategory (Offensive/Defensive) for classification.
- Tools are classified by which category they serve: Garak → Security4AI (Model Robustness), CTF platforms → AI4Security, Inspect → cross-taxonomy.
- Some benchmarks are genuinely dual-use (e.g., WMDP, Zero-day Discovery). List in both directories but add a cross-reference note.

### Factual Accuracy Rules

- **Verify creator attribution** before writing. Common pitfalls we've hit:
  - Cybench → Stanford University (NOT UC Berkeley/UIUC/UChicago)
  - CyberGym → UC Berkeley RDI (NOT Anthropic — they use it but didn't create it)
  - MASK → CAIS, arxiv:2503.03750 (NOT UC Berkeley, NOT 2406.11663)
  - MakeMeSay → OpenAI / Google DeepMind (NOT Redwood Research)
  - CTI-MCQ/CTI-RCM → Rochester IT's CTI-Bench project (NOT Google — Sec-Gemini uses it)
  - AgentHarm → EPFL, Gray Swan, UK AISI, Oxford, CMU (full attribution, not just "UK AISI")
  - Cybench and CyBench are the SAME benchmark. xAI just capitalizes differently.
- **Cross-check numbers** across README, raw-data/, benchmarks/, and cross-comparison.md. The same score must be identical everywhere.
- **87% WMDP for Grok 4.1 is WMDP-Bio**, not WMDP-Cyber. Don't conflate them.

### README Structure Rules

- **Leaderboards come first** in Cross-Comparison (most valuable to users)
- **Group models by company** (OpenAI / Anthropic / Google), not by date
- **Dense reference tables** (Benchmark Mapping, Timeline, Performance Numbers) should be collapsible (`<details>`)
- **Agents section**: Show top 5 picks per category, rest in collapsible list
- **Tools section**: Organize by taxonomy (Security4AI tools / AI4Security platforms / cross-taxonomy frameworks)
- **Don't repeat** information that's already in Cross-Comparison tables in the Benchmarks section — just link to it
- **References section** at the bottom of README consolidates all source documents (system cards, framework docs, papers)

### Entry Format

Every benchmark/agent/tool entry in subdirectories should follow:

```markdown
### [Name](link)
- **Category**: AI4Security > Offensive Capability > CTF
- **Created by**: Organization
- **Used by**: OpenAI, Anthropic, ...
- **Scale**: N tasks/problems
- **Dataset**: Open / Closed / Partial
- **Reference**: [Paper title](arxiv-link)
- **Summary**: One-line description
```

### Style Rules

- Keep descriptions concise — one-liners preferred
- Always include official links (no dead links)
- All performance numbers must include source URL
- Use ✅ / — in comparison tables for readability
- All text must be in English (no Korean)
- Git author must be `ugonfor <ugonfor@gmail.com>` (never hyogon.ryu)

### What NOT to Do

- **No standalone paper entries** — papers are referenced within benchmark/agent/tool entries
- **No general-purpose coding agents** (Claude Code, Codex) — focus on cybersec-specific agents
- **No entries without links** — every name must have an official URL
- **Don't guess arxiv IDs** — verify against the actual paper
- **Don't assume who created a benchmark** — check the paper's author affiliations, not who uses it

## Repo Structure

```
awesome-ai-cybersecurity/
├── README.md                      # Main awesome list (leaderboards, cross-comparison, curated lists)
├── CLAUDE.md                      # This file (behavioral guidelines)
├── raw-data/                      # Vendor documentation analysis (source of truth for numbers)
│   ├── openai.md                  # 19 documents: GPT-4 → GPT-5.3-Codex
│   ├── anthropic.md               # 24 documents: Claude 2 → Claude Opus 4.6
│   ├── google.md                  # 25+ documents: Gemini 1.0 → Gemini 3.1 Pro
│   ├── xai.md                     # 9 documents: Grok-1 → Grok 4.1
│   └── cross-comparison.md        # Detailed cross-comparison (superset of README tables)
├── benchmarks/                    # Individual benchmark entries (70+)
│   ├── ai4security/               # AI helping with cybersecurity
│   │   ├── offensive/             # CTF, pentest, vuln discovery, exploit
│   │   ├── defensive/             # Investigation, SOC, threat intel analysis
│   │   └── knowledge/             # Domain knowledge evaluation
│   └── security4ai/               # Security concerns about AI
│       ├── model-robustness/      # Prompt injection, jailbreak, adversarial
│       ├── misuse-risk/           # AgentHarm, harmful refusal, malware
│       └── alignment/             # Sabotage, deception, sycophancy
├── agents/                        # Cybersecurity AI agents (39)
│   ├── offensive/                 # Pentest agents, CTF solvers, exploit generators
│   ├── defensive/                 # SOC agents, detection/analysis agents
│   └── multi-purpose/
└── tools/                         # Evaluation frameworks, platforms (20)
```

## Data Status (Feb 2026)

- 4 vendor sources collected (77 documents total)
- 70+ benchmarks, 39 agents, 20 tools documented
- 125 URLs verified (2 genuinely broken Google preview links, 22 bot-blocked but browser-accessible)
- Key finding: **virtually no overlap in quantitative benchmarks across companies**
