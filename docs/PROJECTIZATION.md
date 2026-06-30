# Skill 项目化孵化标准

本文件用于判断内部 Skill 是否应升级为可公开、可赞助、可维护的独立 Project。

## 结论先行

不是所有 Skill 都应该变成 Project。Skill 是能力模块，Project 是可被外部用户独立理解、安装、运行、验证、贡献和赞助的产品单元。

**应该项目化的 Skill：** 能解决清晰外部问题、具备可运行代码或可验证工作流、可形成公开路线图、能接受 Issue/PR、能持续迭代。

**不应项目化的 Skill：** 只服务内部口径、依赖私有环境/凭证、只是提示词片段、无法脱敏、无法独立验收、维护成本高于外部价值。

## 项目化六道门

| Gate | 问题 | 通过标准 |
|---|---|---|
| G1 独立价值 | 外部用户不用王国内部上下文也能理解吗？ | README 30 秒讲清楚使用场景、输入输出、收益 |
| G2 可运行性 | 是否有真实代码、CLI、模板或验证脚本？ | 从零 clone 后按 Quickstart 能跑出结果 |
| G3 可验证性 | 是否能用测试/示例/截图证明有效？ | 至少一个 demo、fixture、golden output 或 smoke test |
| G4 可维护性 | 是否有明确 owner、版本、变更记录？ | CODEOWNERS、CHANGELOG、Roadmap、Issue 模板齐全 |
| G5 可合规性 | 是否无私密信息、无外部污染、许可证清晰？ | grep 零命中敏感词；LICENSE/NOTICE 合规 |
| G6 可赞助性 | 用户为什么愿意赞助它？ | 有 Sponsor tiers 对应的维护/功能/支持承诺 |

低于 4 个 Gate：保留为内部 Skill。
通过 4-5 个 Gate：进入 Incubating 项目。
通过 6 个 Gate：升级为 Sponsored-ready 项目。

## 项目成熟度分级

### L0 Internal Skill

- 仅内部使用。
- 可以没有独立仓库。
- 不承诺外部安装体验。

### L1 Incubating Project

必须具备：

- `README.md`：问题、能力、Quickstart、示例、限制。
- `LICENSE`：默认 MIT 或 Apache-2.0；融合外部代码时按源许可证处理。
- `SECURITY.md`：漏洞报告入口。
- `CONTRIBUTING.md`：贡献方式。
- `docs/ROADMAP.md`：未来 3 个里程碑。
- `examples/` 或 `fixtures/`：至少一个可运行样例。

### L2 Production Project

额外具备：

- CI：lint/test/smoke 至少一个 workflow。
- Release：语义化版本 + changelog。
- Typed API 或 CLI help。
- 可复现测试数据。
- 明确兼容性说明。

### L3 Sponsored-ready Project

额外具备：

- GitHub Sponsors 入口。
- 赞助用途说明。
- 公开 Backlog 与 Good First Issues。
- 支持政策：社区支持 vs 赞助支持边界。
- 维护 SLA 不夸大，不承诺无法兑现的响应时间。

## 从 Skill 升级为 Project 的执行流程

1. **读取原 Skill**：必须先读 `SKILL.md`，禁止看名字猜定位。
2. **脱敏扫描**：检查 IP、路径、token、内部代号、用户姓名、群聊链接、Bitable token。
3. **能力拆分**：区分 prompt-only、脚本、模板、数据、私有 SOP。
4. **产品命名**：中文名/英文名/仓库名三者明确，避免混用。
5. **最小可运行包**：先做 Quickstart，不先堆大文档。
6. **验收门禁**：从空目录 clone → 安装 → 运行示例 → 生成结果。
7. **社区治理**：Issue、PR、Security、Support、Funding、Roadmap。
8. **发布**：打 tag，写 release notes，登记到产品矩阵或孵化清单。

## 推荐项目化候选

优先考虑以下类型：

- 有 CLI/脚本的工具型 Skill。
- 可独立解决行业问题的自动化工作流。
- 可公开模板库、检查器、生成器、扫描器。
- 能形成演示站点或示例报告的能力。

暂缓项目化：

- 王国内部角色协作规则。
- 含私有服务器、内部群、客户数据的部署 SOP。
- 只是一段写作风格或个人偏好的提示词。
- 高度依赖当前 Hermes profile 的运行时行为。

## 项目化 PR 必须提供的证据

- `tree -L 3` 或等价目录结构。
- Quickstart 完整执行输出。
- 测试或 smoke test 输出。
- 敏感词 grep 结果。
- 外部来源/许可证说明。
- 是否加入 GitHub Sponsors 的判断。

## 世界领先标准

一个可赞助项目不是“把 Skill 放进仓库”，而是让陌生人能完成五件事：

1. 看懂它解决什么问题。
2. 5 分钟内跑起来。
3. 知道失败时怎么反馈。
4. 能贡献一个小改动。
5. 相信赞助会让项目持续变好。
