# 发现影视官方网站

第一版品牌首页，使用 React 19 + Vite 7，面向专业影视制作、AI 视觉创作和课程介绍。纯前端项目，无需数据库、API 密钥或后端服务。

## 启动与查看

需要 Node.js 22.12+（本环境使用 Node.js 24）。在仓库目录执行：

```bash
npm ci --cache /workspace/.npm-cache
npm run dev -- --port 5173 --strictPort
```

在自己的电脑运行时，在浏览器打开 `http://localhost:5173`。云环境需使用平台的端口预览或转发功能访问 5173 端口；本项目没有公网部署地址。

```bash
npm run build
npm run preview -- --port 4173 --strictPort
```

构建产物在 `dist/`，可部署到支持静态站点的托管平台。生产预览使用 4173 端口。

## 页面与维护

- `src/main.jsx`：首页全部区块、作品数据、筛选、弹窗、移动导航与问答交互。
- `src/styles.css`：深色视觉、响应式布局、动效与减少动态效果偏好。
- `public/images/`：项目制作的本地 SVG 概念演示插画，可替换为获得授权的正式作品素材。
- `public/favicon.svg`：网站图标。
- `index.html`：网页标题、语言、介绍和入口。
- `package.json` / `package-lock.json`：依赖及运行命令，提交锁文件保证安装一致。
- `.gitignore`：排除依赖、构建输出和本地环境文件。

当前只完成首页，通过锚点访问各区块；没有虚构客户、奖项、项目成绩或联系方式。作品均为概念演示，不可播放。课程筹备中，暂不支持报名、支付。联系入口会明确提示联系方式尚未配置，不收集个人信息。

上线前请补充真实联系方式、授权作品与团队资料、正式课程信息，并按实际部署需求添加备案、隐私或其他适用信息。

## 已验证

生产构建；真实 Chromium 浏览器中的作品筛选、详情及课程弹窗、Escape 关闭、问答、移动导航；390 / 768 / 1440 像素宽度无横向溢出。

## 保存到 GitHub

文件已保存在当前云工作区，尚未提交或推送。确认内容后执行：

```bash
git add .gitignore README.md index.html package.json package-lock.json public src
git commit -m "feat: create Faxian Film Studio homepage"
git push origin HEAD:main
```

如果 `main` 有更新或受分支保护，请先协调合并，或推送新分支后创建 Pull Request，勿强制推送。发布云环境配置与提交 GitHub 是不同操作。
