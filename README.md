# xiachenxiashihundan.com

🌐 线上地址：<https://xiaoyang-xy778.github.io/xiachenxiashihundan/>

一个纯静态、零依赖的单页网站 —— 用最严肃的排版，记录最不严肃的控诉。

- 入口文件：`index.html`（HTML + CSS + JS 全部内联，双击即可打开）
- 官方域名（未注册）：`xiachenxiashihundan.com`

## 功能

| 区块 | 说明 |
| --- | --- |
| 首屏 | 渐变 + 故障闪动标题、域名、两个按钮 |
| 六大数据 | 累计控诉人次、已确认罪状、认同度、道歉次数 |
| 六大罪状 | 卡片网格，鼠标跟随光斑、恶劣程度进度条 |
| 受害者证言 | 双向无缝跑马灯，鼠标悬停暂停 |
| 混蛋指数 | 滚动进入视口时数字与进度条动画，封顶 97.3 |
| 和解模式 | 点「算了，原谅他吧」切换暖金配色，标题变为「夏辰骁其实还行」 |

## 交互细节

- 点「我也要控诉」→ 计数 +1（`localStorage` 持久化）+ 表情粒子迸发
- 在线人数每隔几秒跳动一次
- 滚动进场动画基于 `IntersectionObserver`，并带 2.5s 兜底与无 JS 降级
- 支持 `prefers-reduced-motion`，低动效环境下自动关闭动画
- 响应式：桌面三列 → 平板两列 → 手机单列

## 本地预览

直接双击 `index.html`，或起一个静态服务：

```powershell
python -m http.server 8080 --directory .
# 然后打开 http://127.0.0.1:8080/
```

## 部署

任意静态托管即可（GitHub Pages / Cloudflare Pages / Netlify / Vercel / 对象存储），
把 `index.html` 传上去就完事，没有构建步骤、没有外部请求、没有依赖。

## 免责声明

页面内容为朋友之间的玩笑演绎，不构成对任何真实人物的指控、诽谤或人身攻击。
