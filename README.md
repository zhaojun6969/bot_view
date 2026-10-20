# bot_view

本机预先构建的 Deotaland 网站运行产物。不包含项目源码、source map 或 GitHub Actions 构建流程。

## 直接运行

安装 Node.js 22 或更新版本，在此目录执行 npm start，然后打开 http://localhost:4173 。无需 npm install 或 npm run build。

支持 Windows、macOS、Linux。通过 PORT 和 HOST 环境变量修改监听地址，默认 0.0.0.0:4173。

## 邮件订阅

复制 .env.example 为 .env，填写 MAILCHIMP_API_KEY 和 MAILCHIMP_AUDIENCE_ID 后启动。未配置时网站仍可浏览，订阅接口返回暂不可用。不要提交真实密钥。

## 托管

静态托管使用 index.html、assets/、public/。邮件订阅需要同源 /api/subscribe 服务；npm start 已包含此接口。Vercel 配置禁用构建，直接使用静态文件与已打包的 api/subscribe.js，密钥在托管环境配置。

页面中的 Agent 与硬件行为为概念演示。Three.js 许可证见 THREE-LICENSE.txt。
