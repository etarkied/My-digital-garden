<p align="center">
  <img src="src/site/img/cabin-logo.svg" alt="Etar's Note Cabin logo" width="96" height="96">
</p>

# Etar's Note Cabin

我的个人数字花园。本地 [Obsidian](https://obsidian.md) 笔记用
[Digital Garden 插件](https://github.com/oleeskild/Obsidian-Digital-Garden) 发布到本仓库，
再由 Cloudflare Pages 自动构建托管。

> A quiet corner for notes, experiments & half-finished thoughts.

## Where the design lives

| File | What it does |
| --- | --- |
| [`src/site/styles/custom-style.scss`](src/site/styles/custom-style.scss) | 全部视觉：配色、字体、导航栏、文件树、正文、表格、代码、搜索、页脚、响应式 |
| [`src/site/img/cabin-logo.svg`](src/site/img/cabin-logo.svg) | 小屋标志，导航栏 / 文件树 / 404 / 页脚共用 |
| [`src/site/favicon.svg`](src/site/favicon.svg) | 浏览器图标（构建时自动生成 ico / png） |
| [`src/site/_includes/components/navbar.njk`](src/site/_includes/components/navbar.njk) | 无文件树时的顶栏（标志 + 「Etar's Note Cabin」） |
| [`src/site/_includes/components/footer.njk`](src/site/_includes/components/footer.njk) | 站点页脚 |
| [`src/plugins/dg-filetree/templates/filetree.njk`](src/plugins/dg-filetree/templates/filetree.njk) | 左侧文件树里的同款标志 |
| [`.env`](.env) | 站点名、语言、主题开关 |

站点标题由 `.env` 里的 `SITE_NAME_HEADER` 控制，也可在 Obsidian 插件的
**Publication Center → Site → Appearance** 里改「Site name」。

## Notes on the setup

- **Palette**：深色主题取材于 GitHub 深色模式（`#0d1117` 背景 / `#161b22` 卡片 /
  `#30363d` 边框 / `#e6edf3` 文字 / `#58a6ff` 链接），浅色主题对应 GitHub 浅色模式。
  所有颜色都在 `custom-style.scss` 顶部的 `body.theme-dark` / `body.theme-light` 变量块里。
- **Theme**：当前 `.env` 不引用任何 Obsidian 社区主题，因此自定义样式不会被主题覆盖。
  若想让某个主题生效，在 `THEME=` 填入其 `theme.css` 直链即可——
  `custom-style.scss` 里的配色变量在所有主题下都会生效。
- **Logo / Favicon**：仓库自带，无需在插件上传。插件里若上传了自己的图片会优先显示。
- **Updating the template**：`custom-style.scss`、`navbar.njk`、`footer.njk`、
  `cabin-logo.svg` 是本站自行改造的部分，插件升级模板时请保留它们；
  `style.scss`、`digital-garden-base.scss` 仍保持模板原样。

## 本地预览

```sh
npm install
npm run build
# 然后把 dist/ 用任意静态服务器打开，例如：
npx serve dist
```

## Docs

Digital Garden 模板文档：[docs.forestry.md](https://docs.forestry.md/)
