# Auto Claude Code Research in Sleep

A research-workflow toolkit built from Claude Code skill instructions, Python helpers, MCP servers, templates, and examples. It includes tools for literature lookup, experiment/review workflows, and cross-model review. It is not a single unattended research engine, and checked-in files do not prove that a full paper-to-report pipeline runs.

## At a glance

| Area | Repository evidence |
|---|---|
| Skills | 104 `SKILL.md` files in the checked `main` tree on 2026-10-02 |
| Helpers | Python tools for arXiv, Semantic Scholar, review configuration, and task monitoring |
| MCP servers | Claude and Gemini review bridges, plus additional model/chat services |
| Tests | Python tests are present; no test suite was run for this documentation update |
| Setup | No repository-wide installer or root dependency manifest was found in the checked tree |

See the [documentation index](docs/README.md) for guides, MCP server documentation, skills, tools, and tests.

## Start with one workflow

Choose a skill under [`skills/`](skills/) and read its `SKILL.md`, referenced files, and required integrations. For literature lookup, inspect [`tools/arxiv_fetch.py`](tools/arxiv_fetch.py) and its docstring. For task monitoring, review [`tools/watchdog.py`](tools/watchdog.py) and the [watchdog guide](docs/WATCHDOG_GUIDE.md).

The MCP servers have separate setup and credential requirements. Follow their individual guides for [Claude review](mcp-servers/claude-review/README.md) and [Gemini review](mcp-servers/gemini-review/README.md). Do not assume all components are installed or connected.

## Data and provider boundary

Review prompts and supplied research material sent through an MCP bridge are processed by the configured model or CLI provider. Check its data handling terms and access controls before sending unpublished research, personal data, or confidential material. Keep API keys in protected local configuration, not in committed files.

## Validation and limits

- The repository contains documentation, skills, scripts, MCP servers, templates, and tests; they have different prerequisites and are not one integrated package.
- README examples and workflow descriptions are not execution results.
- Do not infer report length, quality, unattended operation, model availability, or zero-cost use from the repository description.
- Run a specific test or workflow only after inspecting its dependencies and effects. No tests, MCP calls, or research jobs were run for this README change.
