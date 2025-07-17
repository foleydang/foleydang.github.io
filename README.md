# HexoBlog Source
这是我的 Hexo 博客源码分支，包含：
- Hexo 配置文件 (`_config.yml`)
- 主题文件 (`themes/`)
- Markdown 文章源文件 (`source/_posts/`)
- 部署脚本（可选）
- `.gitignore` 等管理文件

## 🚀 如何使用

1. 克隆此分支：
   ``` bash
   git clone -b source git@github.com:YOUR_USERNAME/YOUR_REPO.git
   ```

2. 安装依赖：

   ``` bash
   npm install
   ```

3. 本地预览：

   ```bash
   hexo clean
   hexo generate
   hexo server
   ```

   访问：`http://localhost:4000`

4. 部署到远程：
   先在 `_config.yml` 中配置好 `deploy` 部分。
   ```bash
   hexo deploy
   ```

## 📂 分支说明

* `source`：Hexo 源码
* `main`：仅包含 `public/`，即生成好的静态网站文件

## ⚡️ 快速修改

* 新文章：

  ```bash
  hexo new post "My New Post"
  ```
* 生成并部署：

  ```bash
  hexo clean && hexo generate && hexo deploy
  ```

## 📝 说明

* `public/` 目录不会被提交到本分支（已在 `.gitignore` 中）
* 如需还原，请重新 `hexo generate`

---

> 🚧 **本仓库仅作个人备份与演示，内容仅供参考**
