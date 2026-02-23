# CLAUDE.md

## Project Overview

### Repository 헌법
1. 병렬작업이 가능한 것은 agent teams기능을 적극적으로 활용한다.
2. 모든 작업에서 backbone model에 최소한, gemini 3.1 pro, 3 pro, 3 flash, opus 4.6, sonnet 4.6, gpt-5.3-codex, gpt-5.2-codex, grok 4.1, grok 4.1-fast를 포함한다.


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

### PDF Reading Rules (MUST follow)

System card/model card PDF에서 벤치마크 수치를 추출할 때:

1. **Read tool로 직접 PDF를 읽어라** — `Read` tool은 PDF를 시각적으로 렌더링하여 Figure/차트/테이블의 라벨을 정확하게 볼 수 있다. `pages` 파라미터로 페이지 범위를 지정한다 (한번에 최대 20페이지).
2. **`pdftotext`로 차트 수치를 추출하지 마라** — `pdftotext`는 텍스트만 추출하고 차트/Figure 속 라벨은 추출하지 못한다. Agent가 pdftotext 텍스트만 보고 차트 수치를 "추론"하면 hallucination이 발생한다 (실제 사례: GPT-5.3-Codex CTF "77.6% xhigh" — PDF에 존재하지 않는 수치를 agent가 만들어냄).
3. **본문 텍스트에 명시된 수치만 신뢰하라** — Figure/차트의 bar 높이에서 수치를 "읽는" 것은 근사값일 수 있다. 본문에 "scored 0.90" 같이 텍스트로 명시된 수치가 가장 신뢰할 수 있다.
4. **차트에서 읽은 근사값은 `~` 접두사를 붙여라** — 예: WMDP-Bio ~88.2% (차트에서 읽음). 본문 텍스트에서 확인된 수치는 `~` 없이 표기.
5. **Subagent에게 PDF 수치 추출을 맡길 때는 반드시 직접 검증하라** — Agent가 WebFetch나 pdftotext로 작업한 수치는 PDF를 Read tool로 직접 열어 교차 검증해야 한다.

### Data Integrity Rules

- **Never show scores from different benchmarks in the same column without marking which benchmark each score is from.** OpenAI CTF ≠ Google Key Skills ≠ Anthropic RSP CTF. Each column must represent exactly one benchmark.
- **Mark proprietary benchmarks with *(internal)*.** Public benchmarks (Cybench, CVE-Bench, CyberGym, AgentDojo, TAP, Shade) get no label. Internal/proprietary benchmarks (OpenAI Custom CTF, OpenAI Cyber Range, Google Key Skills) get *(internal)* after the column name.
- **Never label public benchmarks with company names.** CVE-Bench is not "OpenAI's CVE-Bench" — it's a public benchmark that OpenAI happens to use. Same for Cybench, CyberGym, AgentDojo, etc.
- **When Misuse Risk and Alignment are separate taxonomy categories, keep them as separate tables.** Don't merge them into a single "Safety" table.
- **Avoid duplicate entries.** Agent Performance Leaderboard should not duplicate with Top Picks. If an agent appears in the Leaderboard, don't repeat it in Top Picks.
- **Collapsible sections for non-core data.** Real-world competitions, third-party evaluations, full performance history, and benchmark mapping should be in `<details>` collapsible sections. Keep the main view clean with only current leaderboard tables.

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
- **GPT-5.3-Codex CTF is 88% (pass@12).** There is NO "77.6% xhigh" score — this was a hallucination from pdftotext-based chart reading.
- **CVE-Bench GPT-5.2-Codex: 87% in own card (40 tasks) vs 85% in GPT-5.3 card (34-task subset).** Both numbers are correct in their respective contexts. Always note which task count applies.
- **Opus 4.5 Cybench: 82% pass@1 (full 40 tasks) vs 79% (RSP 37-task subset).** Both are correct. Always note which task subset is being referenced.
- **Anthropic RSP Cyber CTF categories (Web/Crypto/Pwn/Rev/Network) INCLUDE Cybench tasks** — don't show RSP CTF category breakdowns as a separate benchmark from Cybench. They overlap.

### README Structure Rules

**General layout:**
- **Leaderboards come first** in Cross-Comparison (most valuable to users)
- **Group models by company** (OpenAI / Anthropic / Google / xAI), not by date
- **Dense reference tables** (Benchmark Mapping, Timeline, Performance Numbers) should be collapsible (`<details>`)
- **Don't repeat** information that's already in Cross-Comparison tables in the Benchmarks section — just link to it
- **References section** at the bottom of README consolidates all source documents (system cards, framework docs, papers)

**Taxonomy table:**
- Two columns: **Purpose** + **Benchmarks** (NOT "Meaning" + "Example")

**Leaderboard table rules:**
- **NO Date column** in main leaderboard tables. Date belongs only in collapsible performance history sections.
- All backbone models must appear in every table (see Repository 헌법 #2).

**Specific table structures:**
- **Offensive Capability**: Cybench (shared public) + CTF *(internal)* + Cyber Range *(internal)* columns
- **Vulnerability Discovery**: CVE-Bench + CyberGym + Zero-day columns — this is a SEPARATE table from Offensive Capability
- **Misuse Risk**: Separate table from Alignment (never merge them)
- **Alignment**: Includes Sabotage + Stealth/SA columns
- **Model Robustness**: PI: Coding + PI: Browser + PI: Computer Use + AgentDojo columns

**Agents section:**
- Agent Performance Leaderboard with a **Type** column (Offensive / Defensive / Multi-purpose)
- Top Picks lists only agents NOT already in the Leaderboard — no duplicates

**Tools section:**
- Organize by taxonomy (Security4AI tools / AI4Security platforms / cross-taxonomy frameworks)

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
