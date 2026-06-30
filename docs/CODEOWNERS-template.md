# CODEOWNERS 模板

> 账号级 `.github` 仓无法替所有仓库设置 CODEOWNERS。每个活跃仓需要单独放置 `.github/CODEOWNERS`。

建议模板：

```text
# 默认所有文件由维护团队审阅
* @503496348-ops/maintainers

# 文档
*.md @503496348-ops/docs-maintainers

# 安全与配置
.github/ @503496348-ops/maintainers
SECURITY.md @503496348-ops/maintainers
```

如果当前账号没有 GitHub Team，请改为具体维护者用户名。
