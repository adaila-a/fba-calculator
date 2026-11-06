# Amazon FBA Profit Calculator

一个单文件网页工具：帮亚马逊卖家算清每个产品到底赚不赚钱。

- **技术栈**：纯 HTML + CSS + 原生 JS，零依赖、零构建
- **部署成本**：0 元
- **文件**：只有 `index.html`

---

## 一、本地预览

双击 `index.html` 就能在浏览器里打开。

---

## 二、上线（约 30 分钟）

### 第 1 步：注册 GitHub

1. 打开 https://github.com → Sign up
2. 邮箱注册，用户名用英文

### 第 2 步：新建仓库

1. 右上角 `+` → **New repository**
2. Repository name 填 `fba-calculator`
3. 选 **Public**（Private 也能部署，Public 更省事）
4. 不要勾选 README / .gitignore
5. 点 **Create repository**

### 第 3 步：上传文件

1. 在新仓库页面点 **uploading an existing file**
2. 把 `index.html` 和 `README.md` 拖进去
3. 下面点 **Commit changes**

### 第 4 步：部署到 Vercel

1. 打开 https://vercel.com → **Sign up** → 选 **Continue with GitHub**
2. 授权后点 **Add New… → Project**
3. 找到 `fba-calculator` → **Import**
4. Framework Preset 保持 **Other**，其他都不用改
5. 点 **Deploy**
6. 等约 30 秒，出现 **Congratulations** → 点 **Visit**

你会拿到一个网址，形如：

```
https://fba-calculator-xxxx.vercel.app
```

**这个网址全世界都能打开。** 到这一步，"别人能用"就解决了。

---

## 三、接真实的邮箱收集（5 分钟）

页面底部的邮箱框目前只存在本地浏览器里。要真的收到邮件：

1. 打开 https://formspree.io → 免费注册
2. 新建一个 Form，拿到形如 `https://formspree.io/f/abcdwxyz` 的地址
3. 打开 `index.html`，找到这一行：

```js
var WAITLIST_ENDPOINT = "";
```

4. 把地址填进去：

```js
var WAITLIST_ENDPOINT = "https://formspree.io/f/abcdwxyz";
```

5. 提交到 GitHub（网页上直接编辑 → Commit），Vercel 会自动重新部署

免费额度每月 50 条，验证阶段够用。

---

## 四、绑自己的域名（可选，¥70/年）

1. 去 https://www.cloudflare.com/products/registrar/ 或 https://porkbun.com 买 `.com`
2. Vercel 项目 → **Settings → Domains → Add**
3. 按提示在域名商处加 DNS 记录
4. 生效后把 `index.html` 里的 `example.com` 全部替换成你的域名

---

## 五、上线之后的第一周

**目标不是流量，是判断这个方向值不值得继续。**

| 天 | 做什么 |
|---|---|
| D1 | 自己用 5 个真实产品测试，确认算出来的数对不对 |
| D2 | 发 r/FulfillmentByAmazon（**先认真回答问题，再提工具**，直接发广告会被删） |
| D3 | 发 r/AmazonSeller、r/ecommerce |
| D4 | 提交到 5 个免费工具收录站（搜 "free tool directory submit"） |
| D5–7 | 回评论，记录每条反馈 |

**判断标准：一周内如果有 20+ 个邮箱，说明需求成立，可以继续投入；如果 0–2 个，换方向。**

---

## 六、后续可以做的付费功能

| 功能 | 为什么有人付钱 |
|---|---|
| CSV 批量导入 | 卖家有几十个 SKU，一个个填太慢 |
| 导出 Excel / PDF | 要给合伙人或银行看 |
| 保存历史方案 | 调价后对比 |
| 多平台对比 | 同时算 Amazon / Etsy / TikTok Shop |
| 成本拆分快照 | 分享给供应链同事 |

定价参考：$9/月，或 $49 一次性买断。

---

## 七、费率说明

`index.html` 里的 FBA 配送费和佣金率是**基于亚马逊美国站公开费率的估算值**，用于验证阶段足够，但不保证精确。

正式对外之前，务必对照 Seller Central 的最新费率表核对一遍，并在页面上保留免责声明。

> **提醒**：本工具不构成财务建议。所有费率以亚马逊官方为准。
