# 香港火星文化传媒有限公司 · 官网

Hong Kong Mars Culture Media Limited 企业形象展示站点。**纯静态**：原生 HTML / CSS / JavaScript，无构建工具、无外部 CDN 依赖，可直接部署到任意静态托管平台。

## 业务板块

短剧开发 · 新零售运营 · 直播电商 · 大健康保健品（POPNUTRI 葆力舒 线上独家运营）

## 目录结构

```
hkmars/
├── index.html               # 首页（各板块摘要，链向子页面）
├── about.html               # 公司简介（含发展历程）
├── business.html            # 核心业务（四大板块详解）
├── products.html            # 产品中心（在售产品 + 即将上市 + 销售渠道）
├── product-astaxanthin.html # 产品详情：双抗虾青素胶囊（成分表、技术背书、AstaMAZ 授权书）
├── product-oyster.html      # 产品详情：牡蛎袋鼠精华胶囊（成分表、五大卖点、专利认证）
├── partners.html            # 合作伙伴
├── future.html              # 未来展望（战略方向 + 商业闭环）
├── 404.html                 # 404 兜底页
├── assets/
│   ├── css/style.css   # 全部样式（响应式：1024 / 880 / 640 / 560 断点）
│   ├── js/main.js      # 导航状态、移动端菜单、进场动画、返回顶部
│   ├── favicon.svg     # 站点图标
│   └── img/            # 站点图片素材（来自客户提供 PDF，见 cankao/）
└── cankao/             # 客户原始资料（gitignore，不入仓库）
```

## 本地预览

```bash
cd hkmars
python -m http.server 8080
# 浏览器访问 http://localhost:8080
```

## 部署（GitHub Pages）

1. 推送到 `main` 分支；
2. 仓库 **Settings → Pages → Build and deployment**，Source 选 `Deploy from a branch`，分支选 `main / (root)`，保存；
3. 稍等 1–2 分钟，访问 `https://balloontmz.github.io/hkmars/` 即可。

### 绑定自定义域名（客户购买域名后）

1. 仓库根目录新增 `CNAME` 文件，内容为域名（如 `www.example.com`），提交；
2. 域名解析添加：`www` 的 CNAME 记录指向 `balloontmz.github.io`；或裸域 A 记录指向
   `185.199.108.153` / `185.199.109.153` / `185.199.110.153` / `185.199.111.153`；
3. 在 Settings → Pages → Custom domain 填入域名并开启 **Enforce HTTPS**。

## 内容来源

文案与图片整理自客户提供资料：`mars.pdf`（公司介绍）、`葆力舒品牌介绍.pdf`（产品介绍）。
