# 503496348-ops 公共仓库治理中心

这是 503496348-ops 的账号级 `.github` 默认社区健康仓库，用于为公开项目提供统一的治理骨架。

## 作用范围

当单个仓库没有自带同名文件时，GitHub 会从本仓库继承默认社区健康文件，包括：

- `CONTRIBUTING.md`：贡献与变更流程
- `SECURITY.md`：安全漏洞报告入口
- `SUPPORT.md`：支持与反馈渠道
- `CODE_OF_CONDUCT.md`：协作行为准则
- `.github/ISSUE_TEMPLATE/*`：Issue 模板
- `.github/PULL_REQUEST_TEMPLATE.md`：PR 模板

## 治理原则

1. **默认治理先行**：先用账号级默认文件兜底，避免逐仓复制粘贴。
2. **业务仓保留自主性**：单仓如有特殊流程，可在本仓内覆盖对应文件。
3. **安全与可追溯优先**：所有问题、需求、修复、竞品融合必须留下 Issue/PR 记录。
4. **小步修复，不批量硬改**：仓库改名、归档、迁移等高风险动作必须单独评估。

## 治理文档

- [`docs/PROJECTIZATION.md`](docs/PROJECTIZATION.md)：Skill 是否升级为可公开、可赞助 Project 的六道门。
- [`docs/PRODUCT-QUALITY-GATE.md`](docs/PRODUCT-QUALITY-GATE.md)：公开产品质量门禁，防止空壳仓库和污染残留。
- [`docs/SPONSORSHIP.md`](docs/SPONSORSHIP.md)：GitHub Sponsors 用途、边界和透明度规则。
- [`docs/ROADMAP.md`](docs/ROADMAP.md)：公共治理与 Skill 项目化路线图。
- [`docs/LABELS.md`](docs/LABELS.md)：Issue/PR 标签体系。
- [`docs/CODEOWNERS-template.md`](docs/CODEOWNERS-template.md)：单仓 CODEOWNERS 模板。

## 推荐单仓覆盖清单

每个活跃产品仓最终建议补齐：

- `README.md`
- `LICENSE`
- `SECURITY.md`
- `CONTRIBUTING.md`
- `.github/CODEOWNERS`
- `.github/PULL_REQUEST_TEMPLATE.md`
- `.github/ISSUE_TEMPLATE/bug_report.yml`
- `.github/ISSUE_TEMPLATE/feature_request.yml`
- 至少一个 CI workflow

## Skill 是否要转成 Project？

结论：**要转，但只转能独立运行、公开维护、接受贡献和形成赞助闭环的 Skill。**

- 工具型、检查器、生成器、可演示工作流：优先项目化。
- 内部角色规则、私有部署 SOP、含客户/服务器/群聊上下文的 Skill：保留内部。
- 判断标准以 [`docs/PROJECTIZATION.md`](docs/PROJECTIZATION.md) 的 G1-G6 为准。

## 维护节奏

- 每月：抽样检查活跃仓治理文件覆盖率。
- 每季度：复盘仓库 Topics、归档状态、README 质量、Issue/PR 模板有效性。
- 每次重大产品融合后：检查外部引用清理、许可证合规、安全说明和发布记录。
- 每次 Skill 项目化前：先跑项目化六道门和产品质量门禁。
