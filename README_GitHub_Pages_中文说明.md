# My Website — GitHub Pages 部署说明

## 文件结构

请保持以下文件均位于仓库根目录：

- `index.html`：首页
- `products.html`：产品页
- `about.html`：关于我们
- `contact.html`：联系我们
- `Home_files/`、`Products_files/`、`About_files/`、`Contact_files/`：页面所需图片、CSS 和 JavaScript
- `.nojekyll`：告诉 GitHub Pages 不运行 Jekyll 处理

不要只上传外层文件夹；应将 ZIP 内的这些文件和文件夹直接放到 GitHub 仓库根目录。

## 发布步骤

1. 在 GitHub 创建一个新仓库，例如 `my-website`。
2. 建议先将仓库设为 Public（GitHub Free 的 Pages 网站要求公开仓库）。
3. 解压本 ZIP，把解压后根目录里的所有文件和文件夹上传到仓库根目录并提交。
4. 打开仓库 `Settings` → `Pages`。
5. 在 `Build and deployment` 中选择 `Deploy from a branch`。
6. Branch 选择 `main`，Folder 选择 `/(root)`，点击 `Save`。
7. 等待部署完成，在 Pages 页面点击 `Visit site`。

## 重要说明

- GitHub Pages 是静态托管，适合 HTML、CSS、JavaScript 和图片；不运行 PHP、Python 等服务器端代码。
- 当前 Contact 联系表单仍依赖原网站编辑器的 `/api/contact/` 后端接口。GitHub Pages 没有该接口，因此需要将表单改接 Formspree、Getform 等第三方表单服务，或接入自己的后端后，才可正常接收邮件。
- 页面中保留了原网站的 canonical SEO 地址（`promoonly.com.cn`）。如果最终使用 `github.io` 地址，应将各 HTML 文件中的 canonical 地址更新为最终网址；若最终继续使用原自有域名，则应确认该域名确实指向最终发布的网站。
- 字体文件没有完整包含在原始 ZIP 中，某些字体可能显示为浏览器替代字体。
- 上传前请确认仓库中没有密码、私密文件、客户资料或其他不应公开的信息。GitHub Pages 网站是公开可访问的。

## 更新网站

以后修改网页或图片后，将修改后的文件提交（Commit）并推送到 `main` 分支，GitHub Pages 会自动重新部署。
