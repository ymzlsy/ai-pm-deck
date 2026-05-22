# AI 时代产品经理的工作模式 — 网页演示

笔记本 Tab 风格 HTML 幻灯片，单文件 `index.html`。

- 线上（当前可用）：https://ymzlsy.github.io/ai-pm-deck/
- 自定义域（待 DNS）：https://ai-pm.karaithy.com/

### 绑定 `ai-pm.karaithy.com`（Cloudflare DNS 一步）

在 [Cloudflare DNS](https://dash.cloudflare.com/) 选择 `karaithy.com` → 添加记录：

| 类型 | 名称 | 目标 | 代理 |
|------|------|------|------|
| CNAME | `ai-pm` | `ymzlsy.github.io` | **仅 DNS**（灰云，关闭代理） |

然后在仓库根目录恢复 `CNAME` 文件（内容为 `ai-pm.karaithy.com`），并在 GitHub → Settings → Pages 填写 Custom domain。HTTPS 生效约 10–30 分钟。

本地预览：`python3 -m http.server 8766 --bind 127.0.0.1`
