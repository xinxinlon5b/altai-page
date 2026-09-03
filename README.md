# altai-page（企业 AI 落地伙伴 · 公开学习地图）

> 本项目为**唯一对外网页**：`companion.html`
> 架构原则：**一个 Agent（Hermes/EAC）当大脑 + 一个网页当窗口**。网页只负责展示脱敏结论，思考/记忆/主动学习都在 agent 侧完成。

## 对外入口

| 地址 | 说明 |
|---|---|
| https://xinxinlon5b.github.io/altai-page/ | 根路径（自动跳转 companion.html） |
| https://xinxinlon5b.github.io/altai-page/companion.html | **唯一对外窗口** |

## 仓库结构说明

- `companion.html` — 唯一对外展示页（14 子领域/经验时间线/决策卡/方法论）
- `index.html` — 自动重定向到 companion.html（保留根路径友好）
- 其余 `.html`（architecture / methodology / review / roadmap / systems / value / architect-helper / docker_* 等）— **历史演进存档，不再对外链接**，git 历史完整可查。不要新建对外页面；新增内容一律进 companion.html 或交给 agent 会话。

## 更新规则（给 agent 的）

- 改完必须本地验证（`python3 -m http.server` 或 file:// 打开）+ push 后轮询线上 200
- 中文全部 UTF-8；JS 字符串里中文引号用「」避免破坏语法
- 公开页只放脱敏结论；原始证据（Obsidian 路径/截图/链接）留本机
- 数据更新优先走数据驱动（companion.html 内 LESSONS / MAP / FLYWHEEL / decisions），别改结构