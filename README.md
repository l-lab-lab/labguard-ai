# LabGuard AI Cloudflare Pages 部署包

本目录是可直接部署到 Cloudflare Pages 的静态演示版。

## 部署

1. 将本目录中的 `index.html` 与 `_headers` 上传到一个 GitHub 仓库。
2. 登录 Cloudflare Dashboard，进入 **Workers 和 Pages** → **创建** → **Pages** → **连接到 Git**。
3. 选择该 GitHub 仓库；框架预设选择 `None`，构建命令留空，输出目录填写 `/`。
4. 点击部署，即可获得 `*.pages.dev` 公网网址；之后可在 Pages 的 Custom domains 绑定自己的域名。

## 说明

这是比赛演示型静态版本：预约、AI 预审、审批、看板均在浏览器运行；演示数据保存在每位访问者自己的浏览器 localStorage 中，不会共享给其他访问者。

如需多人使用同一份数据，应将后端迁移为 Cloudflare Workers + D1 数据库，再部署到同一 Cloudflare 账户。
