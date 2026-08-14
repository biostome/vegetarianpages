# GitHub Pages 部署说明（隐私政策 & 技术支持）

## 本目录包含

| 文件 | 用途 | 部署后 URL |
| --- | --- | --- |
| `privacy-policy.html` | 隐私政策（已去掉联系方式） | `https://<你的用户名>.github.io/<仓库名>/privacy-policy.html` |
| `support.html` | 技术支持页面（不含联系方式） | `https://<你的用户名>.github.io/<仓库名>/support.html` |

## 部署步骤

1. 在 GitHub 上**新建一个公开仓库**（例如 `suvegmap-support`），不要勾选"Add a README"（保持空仓库）。
2. 把本目录下的两个文件上传到仓库：
   - 网页端：进入仓库 → `Add file → Upload files`，选择这两个文件 → Commit。
   - 或命令行：
     ```bash
     cd docs/release/github-pages
     git init
     git add .
     git commit -m "privacy policy and support pages"
     git remote add origin https://github.com/<你的用户名>/<仓库名>.git
     git push -u origin main
     ```
3. 进入仓库 **Settings → Pages**：
   - Source 选择 **Deploy from a branch**
   - Branch 选择 `main`，目录选 `/ (root)`
   - 点击 **Save**
4. 等待 1-3 分钟，页面顶部会显示 `Your site is live at https://<你的用户名>.github.io/<仓库名>/`。
5. 打开以下地址确认可访问：
   - `https://<你的用户名>.github.io/<仓库名>/privacy-policy.html`
   - `https://<你的用户名>.github.io/<仓库名>/support.html`

## 注意事项

- **仓库必须公开**，GitHub Pages 不支持私有仓库（免费版）。
- 若提示"网站已发布但没有页面"，等待 1 分钟刷新即可。
- 两个页面互相有链接（support.html 里链接到 privacy-policy.html），放在同一仓库同一目录即可正常跳转。

## 部署完成后

将最终的两个 URL 填入 App Store Connect：

| 字段 | 填写 |
| --- | --- |
| 支持网址 (Support URL) | `https://<你的用户名>.github.io/<仓库名>/support.html` |
| 隐私政策网址 (Privacy Policy URL) | `https://<你的用户名>.github.io/<仓库名>/privacy-policy.html` |
