# CLAUDE.md

## Project Overview

**awesome-ai-cybersecurity** — A curated list of AI cybersecurity benchmarks, agents, and tools, organized by a clear taxonomy.

- GitHub: https://github.com/ugonfor/awesome-ai-cybersecurity
- Scope: Benchmarks, Agents/Tools (NO papers-only entries — papers are linked as references within entries)
- Target companies/models: OpenAI, Anthropic (Claude), Google (Gemini), xAI (Grok) and beyond

## Core Taxonomy: The "OF / BY / FROM" Framework

The key differentiator of this repo. The AI cybersecurity space conflates red team, blue team, safety, and security. We cut through the confusion with two axes:

### Axis 1: Whose security?

| Category | Meaning | Example |
|----------|---------|---------|
| **Security OF AI** | Protecting the AI model itself | Jailbreak defense, prompt injection robustness |
| **Security BY AI** | AI performing cybersecurity tasks | CTF solving, vulnerability analysis, SOC automation |
| **Security FROM AI** | Assessing risks posed by AI | Malware generation capability, exploit writing risk |

### Axis 2: Offensive vs Defensive

| Category | Meaning |
|----------|---------|
| **Offensive (Red Team)** | Attack simulation, vulnerability discovery |
| **Defensive (Blue Team)** | Detection, analysis, incident response |
| **Evaluation** | Pure capability measurement (no attack/defense distinction) |

## Repo Structure

```
awesome-ai-cybersecurity/
├── README.md                      # Main awesome list (cross-comparison, benchmark mapping, performance numbers)
├── CLAUDE.md                      # This file (project guidelines for AI assistants)
│
├── raw-data/                      # Collected vendor documentation analysis
│   ├── openai.md                  # 19 documents: GPT-4 → GPT-5.3-Codex
│   ├── anthropic.md               # 24 documents: Claude 2 → Claude Opus 4.6
│   ├── google.md                  # 25+ documents: Gemini 1.0 → Gemini 3.1 Pro
│   ├── xai.md                     # 9 documents: Grok-1 → Grok 4.1
│   └── cross-comparison.md        # Detailed cross-comparison (superset of README tables)
│
├── benchmarks/                    # (TODO) Individual benchmark entries
│   ├── security-of-ai/            # Jailbreak, prompt injection, adversarial robustness
│   ├── security-by-ai/            # CTF, pentest, code audit, detection benchmarks
│   │   ├── offensive/
│   │   ├── defensive/
│   │   └── knowledge/
│   └── security-from-ai/          # Misuse risk, dual-use, WMDP-style
│
├── agents/                        # (TODO) Cybersecurity AI agents
│   ├── offensive/                 # Pentest agents, CTF solvers, exploit generators
│   ├── defensive/                 # SOC agents, detection/analysis agents
│   └── multi-purpose/
│
└── tools/                         # (TODO) Evaluation frameworks, platforms
```

## Entry Format Convention

Every benchmark/agent/tool entry should follow this format:

```markdown
### [Name](link)
- **Category**: Security BY AI > Offensive > CTF
- **Created by**: Organization
- **Used by**: OpenAI, Anthropic, ...
- **Scale**: N tasks/problems
- **Dataset**: Open / Closed / Partial
- **Reference**: [Paper title](arxiv-link)
- **Summary**: One-line description
```

## Key Decisions

- **No standalone paper entries**: Papers are referenced within benchmark/agent/tool entries, not listed separately
- **Agents & tools ARE in scope**: Custom cybersec AI agents (PentestGPT, etc.), not just benchmarks
- **Commercial tools (Claude Code, Codex) are OUT of scope**: Focus on cybersec-specific agents
- **Taxonomy-first approach**: The OF/BY/FROM classification is the repo's core value proposition
- **Cross-comparison lives in README**: The benchmark mapping and performance numbers are the README's centerpiece
- **Raw data in raw-data/**: Detailed per-vendor analysis with all source URLs preserved

## Data Collection Status

All 4 vendor sources have been collected and analyzed (as of Feb 2026):

- **OpenAI**: 19 system cards/reports mined. Key benchmarks: Custom CTF, CVE-Bench, Cyber Range
- **Anthropic**: 24 documents mined. Key benchmarks: Cybench, CyberGym, CMU Cyber Ranges, real CTF competitions
- **Google**: 25+ documents mined. Key benchmarks: InterCode-CTF, In-house CTF, Hack the Box, Key Skills, Pattern Labs
- **xAI**: 9 documents mined. Key benchmarks: CyBench, WMDP-Cyber, AgentHarm, AgentDojo

Key finding: **virtually no overlap in quantitative benchmarks across companies**.

## TODO

- [ ] Fill in individual benchmark entries (benchmarks/ directory)
- [ ] Research and add cybersecurity AI agents (agents/ directory)
- [ ] Research and add evaluation tools/frameworks (tools/ directory)
- [ ] Verify all URLs in raw-data/ are live (link checking)
- [ ] Add academic benchmarks not used by the 4 companies (CyberSecEval, SecBench, CyberMetric, HarmBench, etc.)

## Style Guide

- Keep descriptions concise — one-liners preferred
- Always include official links (no dead links)
- Use the taxonomy categories consistently
- All performance numbers must include source URL
- Use ✅ / — in comparison tables for readability
