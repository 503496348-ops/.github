# Repository Label Taxonomy

统一标签用于让 Issue、PR、项目化候选和维护状态可检索、可统计、可自动化。

## 类型标签

| Label | 用途 |
|---|---|
| `type: bug` | 已确认或疑似缺陷 |
| `type: feature` | 新能力请求 |
| `type: docs` | 文档、示例、说明改进 |
| `type: refactor` | 不改变行为的结构调整 |
| `type: security` | 安全、依赖、敏感信息问题 |
| `type: governance` | 仓库治理、模板、流程 |
| `type: projectization` | Skill 升级为 Project 相关事项 |

## 优先级标签

| Label | 含义 |
|---|---|
| `priority: p0` | 阻断使用、安全事故、数据泄露风险 |
| `priority: p1` | 重要缺陷或关键体验问题 |
| `priority: p2` | 正常迭代 |
| `priority: p3` | 低优先级优化 |

## 状态标签

| Label | 含义 |
|---|---|
| `status: needs-triage` | 待分诊 |
| `status: needs-info` | 等待补充信息 |
| `status: accepted` | 已接受，等待实现 |
| `status: blocked` | 被外部依赖阻塞 |
| `status: sponsored-ready` | 已达到可赞助项目标准 |
| `status: internal-only` | 不适合公开项目化 |
| `status: archived` | 计划归档或已归档 |

## 领域标签

| Label | 用途 |
|---|---|
| `area: frontend` | 前端、UI、可视化 |
| `area: backend` | 后端、API、数据库 |
| `area: ai-agent` | Agent、Skill、自动化工作流 |
| `area: security` | 安全扫描、凭证、供应链 |
| `area: docs` | 文档与教程 |
| `area: ops` | 部署、CI/CD、仓库治理 |

## 贡献者标签

| Label | 用途 |
|---|---|
| `good first issue` | 适合首次贡献 |
| `help wanted` | 需要外部协助 |
| `discussion` | 需要方案讨论，不应直接开工 |

## 建议批量创建命令

在具体仓库中执行：

```bash
gh label create "type: bug" --color D73A4A --description "Bug or regression" || true
gh label create "type: feature" --color A2EEEF --description "New capability" || true
gh label create "type: docs" --color 0075CA --description "Documentation" || true
gh label create "type: security" --color B60205 --description "Security issue" || true
gh label create "type: projectization" --color 5319E7 --description "Skill-to-project work" || true
gh label create "priority: p0" --color B60205 --description "Critical" || true
gh label create "priority: p1" --color D93F0B --description "High" || true
gh label create "priority: p2" --color FBCA04 --description "Medium" || true
gh label create "priority: p3" --color C2E0C6 --description "Low" || true
gh label create "status: needs-triage" --color FEF2C0 --description "Needs triage" || true
gh label create "status: sponsored-ready" --color 0E8A16 --description "Ready for sponsorship" || true
gh label create "status: internal-only" --color BFDADC --description "Not suitable for public projectization" || true
```

不要在未读仓库内容前批量打领域标签。领域标签必须基于 README/SKILL/source evidence。
