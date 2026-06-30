# Product Quality Gate

本门禁用于防止“空壳产品”“README 伪装产品”“竞品污染残留”和“不可运行项目”进入公开产品矩阵。

## P0：公开前必须通过

| Gate | 检查 | 通过标准 |
|---|---|---|
| README | 是否解释问题、安装、使用、示例、限制 | 陌生用户能 5 分钟跑通 Quickstart |
| LICENSE | 是否存在且与来源兼容 | LICENSE 文件存在；融合代码保留必要 NOTICE |
| SECURITY | 是否有漏洞报告入口 | SECURITY.md 存在或继承账号默认文件 |
| Run | 是否真实可运行 | smoke test / CLI help / demo 至少一种真实输出 |
| Secrets | 是否无密钥泄露 | grep 无 token/password/api_key/private key |
| Pollution | 是否无外部污染 | grep 无“融合自/原作者/Stars/GitHub URL/外部变量名”残留 |

## P1：成熟项必须补齐

- CI workflow 至少一个。
- CHANGELOG 或 GitHub Releases。
- Issue/PR 模板。
- CODEOWNERS。
- examples 或 fixtures。
- docs/ROADMAP.md。
- Topics 与 Description 标准化。

## P2：Sponsored-ready 加分项

- Good First Issues。
- 赞助用途说明。
- 支持边界说明。
- 项目成熟度徽章或状态说明。
- 可复现 benchmark 或示例报告。

## 标准验证命令

```bash
# 基础结构
for f in README.md LICENSE SECURITY.md CONTRIBUTING.md; do [ -f "$f" ] && echo "OK $f" || echo "MISS $f"; done

# 敏感信息
if grep -RInE 'sk-[A-Za-z0-9]|api[_-]?key|token=|password=|private key|BEGIN .*PRIVATE KEY' . --exclude-dir=.git; then
  echo "FAIL secrets"
else
  echo "OK no obvious secrets"
fi

# 外部污染
if grep -RInE '融合自|原作者|合并自|adapted from|forked from|[0-9]+(\.[0-9]+)?K⭐|github.com/.+/.+' . --exclude-dir=.git; then
  echo "CHECK pollution candidates"
else
  echo "OK no obvious pollution"
fi

# Python 项目
python3 -m compileall .

# Node 项目
npm test || npm run build || npm run lint
```

## 禁止交付

- 只更新 README，不提供可运行证据。
- 只看仓库名就分类。
- 竞品融合后不清理来源、作者名、Stars 和变量名。
- 把内部路径、服务器名、Bitable token、群聊链接写进公开文档。
- 没有 license 判断就复制外部代码。

## 交付报告格式

每个公开项目交付时必须给出：

```text
项目：
仓库：
成熟度：L0/L1/L2/L3
本次变更：
验证命令与输出：
未完成风险：
下一步：
```
