# AI 时代产品经理的工作模式 — 网页演示

笔记本 Tab 风格 HTML 幻灯片，单文件 `index.html`。

- **对外分享**：https://ai-pm.karaithy.com/
- **说明**：`*.pages.dev` 是 Cloudflare 每个 Pages 项目自带的临时地址，不是最终域名；与 `wiki.karaithy.com`、`travmini-admin.karaithy.com` 一样，正式访问应用 `ai-pm.karaithy.com`。

### 完成 `ai-pm.karaithy.com`（Cloudflare DNS 一步）

Pages 项目已创建并绑定域名，还差 DNS 记录。在 [Cloudflare DNS](https://dash.cloudflare.com/) → `karaithy.com` → 添加：

| 类型 | 名称 | 目标 | 代理 |
|------|------|------|------|
| CNAME | `ai-pm` | `ai-pm-deck.pages.dev` | 已代理（橙云）即可 |

保存后约 2–5 分钟可访问。后续更新：在 `ppt-notebook/` 目录执行 `npx wrangler pages deploy . --project-name=ai-pm-deck --branch=main`

本地预览：`python3 -m http.server 8766 --bind 127.0.0.1`

### `demo/` 目录（数字人案例页依赖）

| 目录 | 说明 |
|------|------|
| `demo/digital-human-doc/` | 对外演示文档（幻灯片 iframe 主入口） |
| `demo/digital-human-xiaoan/` | 「小安」在线交互（doc 内嵌 `../digital-human-xiaoan/index.html`） |

源项目路径：`~/Desktop/ja_project/260506-shenyang/demo/`（与飞书 page6 指引的 `deliverables/digital-human-demo-for-leader` 同源）。更新演示文档后在该目录改，再 `rsync` 到本仓库 `demo/`。部署时需一并上传两个子目录，否则「在线交互体验」会 404。

Part2 新增页（飞书 page7–9）：前端代码输出、产品产出可用、Hermes 截图（`images/hermes-*.png`，来自飞书大纲附图）。
