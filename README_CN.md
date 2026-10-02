# Auto Claude Code Research in Sleep

本仓库收录科研工作流相关的 Claude Code skills、Python 辅助工具、MCP 服务、模板和示例，涉及文献检索、实验与评审流程，以及跨模型评审。它不是一个已验证的无人值守科研引擎；仓库中的文件也不能证明完整的论文到报告流程可以运行。

## 仓库内容

| 内容 | 当前仓库证据 |
|---|---|
| Skills | 截至 2026-10-02 的 `main` 树中有 104 个 `SKILL.md` 文件 |
| 辅助工具 | arXiv、Semantic Scholar、评审配置和任务监控相关的 Python 工具 |
| MCP 服务 | Claude 与 Gemini 评审桥接，以及其他模型聊天服务 |
| 测试 | 仓库中有 Python 测试；本次文档更新未运行测试 |
| 安装 | 检查的目录中没有统一安装脚本或根目录依赖清单 |

查看[文档索引](docs/README.md)，了解指南、MCP 服务、skills、工具和测试的位置。

## 从单个工作流开始

先选用 [`skills/`](skills/) 下的 skill，并阅读它的 `SKILL.md`、引用文件和依赖。文献检索可先查看 [`tools/arxiv_fetch.py`](tools/arxiv_fetch.py) 及其说明。任务监控可先阅读 [`tools/watchdog.py`](tools/watchdog.py) 和[监控指南](docs/WATCHDOG_GUIDE.md)。

MCP 服务有各自的安装和凭证要求。请分别阅读 [Claude 评审桥接](mcp-servers/claude-review/README.md)和 [Gemini 评审桥接](mcp-servers/gemini-review/README.md)，不要假定所有组件都已安装或连接。

## 数据与模型服务边界

通过 MCP 桥接发送的评审提示词和研究材料会交由配置的模型或命令行服务处理。发送未发表研究、个人数据或机密资料前，请先检查相应服务的数据处理条款和访问控制。API 密钥应保存在受保护的本地配置中，不要提交到仓库。

## 验证范围与限制

- 仓库包含文档、skills、脚本、MCP 服务、模板和测试；各部分有不同依赖，不是一个统一软件包。
- README 示例和工作流描述不等于实际运行结果。
- 不应仅凭仓库描述推断报告长度、研究质量、无人值守能力、模型可用性或零成本。
- 运行具体测试或工作流前，先检查其依赖和副作用。本次 README 更新没有运行测试、MCP 请求或科研任务。
