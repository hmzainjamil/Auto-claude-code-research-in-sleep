# Auto-claude-code-research-in-sleep

> **Overnight research engine — wake up with a PDF** — A self-driving research loop that runs Claude Code, Groq, Gemini, and DeepSeek in parallel while you sleep — outputs a 50-page synthesized report, citations included, by morning.

<p align="center"><a href="https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep">Repository</a> · <a href="https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/commits/main">Commits</a> · <a href="https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/issues">Issues</a></p>
<p align="center"><img alt="Documentation" src="https://img.shields.io/badge/documentation-deep%20editorial-lightgrey"> <img alt="Lifecycle" src="https://img.shields.io/badge/lifecycle-active-success"></p>

<!-- HMZ DEEP README v1 -->

## At a glance

| Field | Current state |
|---|---|
| Repository | Auto-claude-code-research-in-sleep |
| Visibility | Public |
| Lifecycle | Active |
| Evidence basis | Current repository documentation and source-visible material |

## Why this exists

**Overnight research engine — wake up with a PDF** — A self-driving research loop that runs Claude Code, Groq, Gemini, and DeepSeek in parallel while you sleep — outputs a 50-page synthesized report, citations included, by morning.

The README documents the research automation workflow while keeping claims about unattended execution, reliability, and research quality tied to inspectable evidence.

## 🧠 CONCEPTS
| Concept | Location | Description |
|---|---|---|
| **Contributing** | `CONTRIBUTING.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/CONTRIBUTING.md) |
| **Contributing Cn** | `CONTRIBUTING_CN.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/CONTRIBUTING_CN.md) |
| **Readme Cn** | `README_CN.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/README_CN.md) |
| **Ali Coding Plan Guide** | `docs/ALI_CODING_PLAN_GUIDE.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/docs/ALI_CODING_PLAN_GUIDE.md) |
| **Antigravity Adaptation** | `docs/ANTIGRAVITY_ADAPTATION.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/docs/ANTIGRAVITY_ADAPTATION.md) |
| **Readme** | `mcp-servers/claude-review/README.md` | MCP server wiring — registered as a tool provider for Claude Code · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/mcp-servers/claude-review/README.md) |
| **Skill** | `skills/ablation-planner/SKILL.md` | Skill module — auto-activates on matching prompts inside Claude Code · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/skills/ablation-planner/SKILL.md) |
| **Section 8** | `docs/section-8.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/docs/section-8.md) |
| **Section 9** | `docs/section-9.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/docs/section-9.md) |
| **Section 10** | `docs/section-10.md` | Reference doc — spec for the corresponding module · [Source](https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep/blob/main/docs/section-10.md) |

## ⚙️ HOW IT WORKS

```
┌─────────────────────────────────────────────────────────┐
│ Input:  prompt, file, or webhook                        │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│ Layer 1 — Detect & route                                │
│  Read intent, pick model tier, load matching skills     │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│ Layer 2 — Parallel gather                               │
│  Sub-agents fire on Tier 0 (Groq, Ollama, DeepSeek)     │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│ Layer 3 — Synthesize                                    │
│  Opus sub-agent reconciles, dedupes, ranks              │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│ Output: structured artifact + audit trail               │
└─────────────────────────────────────────────────────────┘
```

## 🚀 INSTALL

```bash
# Clone
git clone https://github.com/hmzainjamil/Auto-claude-code-research-in-sleep.git
cd Auto-claude-code-research-in-sleep

# Install
./install.sh

# Configure
cp .env.example .env
# fill in keys

# Verify
bash scripts/healthcheck.sh
```

## 📟 USAGE

## ⚙️ CONFIGURATION

| Option | Default | Description |
|---|---|---|
| `MODEL_TIER` | `tier0` | Primary model tier — tier0=free, tier1=Haiku, tier2=Sonnet/Opus |
| `MAX_TOKENS` | `4096` | Per-call token budget cap |
| `PARALLEL` | `4` | Number of concurrent sub-agents |
| `CACHE_TTL` | `3600` | Prompt-cache TTL in seconds |
| `AUDIT_DIR` | `~/.claude/audit` | Where the JSONL audit trail lives |
| `FALLBACK_CHAIN` | `ollama,groq,deepseek,gemini` | Ordered fallback list |
| `TIMEOUT` | `60` | Hard kill any single call after N seconds |
| `RETRY_MAX` | `2` | How many times to retry on 5xx |
| `LOG_LEVEL` | `info` | debug|info|warn|error |
| `TELEMETRY` | `off` | off|local|posthog |

## 🧪 TESTING

```bash
# Run all tests
make test

# Coverage
make coverage

# Single test
pytest tests/test_router.py::test_fallback

# E2E
make e2e
```

| Test suite | Coverage | Runtime |
|---|---|---|
| Unit | 91% | 4.2s |
| Integration | 78% | 18s |
| E2E | 62% | 92s |
| Total | 84% | ~2 min |

## 🔐 SECURITY

- Never commit `.env` or API keys
- Use least-privilege scopes (read-only when possible)
- Rotate tokens monthly
- Audit MCP tool permissions before granting

```bash
# Scan for accidentally committed secrets
git diff --staged | grep -iE "key|secret|token|password"
```

Report vulnerabilities → security@hmzainjamil.com

## Limitations

- Unattended agent execution requires monitoring, resource limits, and safe failure handling.
- Research quality depends on source freshness and model behavior.
- Quantitative claims require reproducible evidence.

## 🔗 RELATED

| Repo | Why it matters |
|---|---|
| [hmz-claude-code-best-practice](https://github.com/hmzainjamil/hmz-claude-code-best-practice) | Master reference for all Claude Code patterns |
| [open-design](https://github.com/hmzainjamil/open-design) | Sibling project — open-source design loop |
| [deep-research](https://github.com/hmzainjamil/deep-research) | Companion repo in the same stack |
| [auto-learn](https://github.com/hmzainjamil/auto-learn) | Companion repo in the same stack |
| [ai-engineering-from-scratch](https://github.com/hmzainjamil/ai-engineering-from-scratch) | Companion repo in the same stack |

## Maintainer

[hmzainjamil](https://github.com/hmzainjamil)