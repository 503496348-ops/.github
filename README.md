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

## 维护节奏

- 每月：抽样检查活跃仓治理文件覆盖率。
- 每季度：复盘仓库 Topics、归档状态、README 质量、Issue/PR 模板有效性。
- 每次重大产品融合后：检查外部引用清理、许可证合规、安全说明和发布记录。
