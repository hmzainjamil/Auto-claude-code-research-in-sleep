# Documentation index

Repository map for the research workflow toolkit. Verify dates and provider behavior against current source and official service documentation.

| Area | Entry points | Scope |
|---|---|---|
| Overview | [English README](../README.md), [中文 README](../README_CN.md) | Repository purpose, evidence, data boundary |
| Skills | [Skill folders](../skills/) | Each `SKILL.md` defines its own instructions and dependencies |
| Literature tools | [arXiv helper](../tools/arxiv_fetch.py), [Semantic Scholar helper](../tools/semantic_scholar_fetch.py) | Python source; inspect before use |
| Monitoring | [Watchdog source](../tools/watchdog.py), [watchdog guide](WATCHDOG_GUIDE.md) | Server task/GPU monitoring |
| MCP review | [Claude review](../mcp-servers/claude-review/README.md), [Gemini review](../mcp-servers/gemini-review/README.md) | Provider-specific setup and review bridges |
| Other MCP services | [MCP server folders](../mcp-servers/) | Check each server's source and requirements |
| Workflow guides | [Project files](PROJECT_FILES_GUIDE.md), [session recovery](SESSION_RECOVERY_GUIDE.md), [watchdog](WATCHDOG_GUIDE.md) | Historical procedure docs; verify against the current files |
| Research examples | [Narrative report example](NARRATIVE_REPORT_EXAMPLE.md), [templates](../templates/) | Example outputs and reusable templates |
| Tests | [Python tests](../tests/) | Present in source; results are not asserted here |
| Contribution | [English](../CONTRIBUTING.md), [中文](../CONTRIBUTING_CN.md) | Contribution guidance |

The repository does not have a single root installer or universal runtime command. Setup is component-specific. Treat dated guides and external model claims as time-sensitive.
