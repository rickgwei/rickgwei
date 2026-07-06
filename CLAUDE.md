# CLAUDE.md

本仓库是 Rick 的 **GitHub 个人主页仓库**(`github.com/rickgwei/rickgwei`)。`README.md` 就是产物——它是对外门面,**没有构建步骤**。

## 自动化:博客文章自动同步

`.github/workflows/update-blog-posts.yml` 每 6 小时 cron 运行:用 Python3 解析博客 RSS(`https://rickgwei.com/en/index.xml`),取最新 5 篇,替换 `README.md` 中 `<!-- BLOG-POSTS:START -->` 与 `<!-- BLOG-POSTS:END -->` 之间的内容,并自动提交 `chore: sync latest blog posts`。

## 编辑约定

- **不要手动编辑 `BLOG-POSTS:START/END` 标记之间的内容**——会被下一次 cron 覆盖。
- 其余部分(bio、当前项目、链接、社交媒体)可手动编辑。

## 关键文件

- `README.md` — 唯一产物
- `.github/workflows/update-blog-posts.yml` — RSS 自动同步流水线
