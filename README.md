# AI 时代产品经理的工作模式 — 网页演示

笔记本 Tab 风格 HTML 幻灯片，单文件 `index.html`。

- **主链接（Cloudflare Pages）**：https://ai-pm-deck.pages.dev/
- **自定义域（绑定中）**：https://ai-pm.karaithy.com/
- **备用（GitHub Pages）**：https://ymzlsy.github.io/ai-pm-deck/

### 完成 `ai-pm.karaithy.com`（Cloudflare DNS 一步）

Pages 项目已创建并绑定域名，还差 DNS 记录。在 [Cloudflare DNS](https://dash.cloudflare.com/) → `karaithy.com` → 添加：

| 类型 | 名称 | 目标 | 代理 |
|------|------|------|------|
| CNAME | `ai-pm` | `ai-pm-deck.pages.dev` | 已代理（橙云）即可 |

保存后约 2–5 分钟可访问。后续更新：在 `ppt-notebook/` 目录执行 `npx wrangler pages deploy . --project-name=ai-pm-deck --branch=main`

本地预览：`python3 -m http.server 8766 --bind 127.0.0.1`
