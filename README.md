<h1 align="center">
    LapisCV
</h1>
<p align="center">
    📃 开箱即用的 Markdown 简历，支持 VSCode / Obsidian / Typora
</p>
<div align="center">
    <img alt="Release" src="https://img.shields.io/github/v/release/BingyanStudio/LapisCV?style=flat-square&color=1694b6">
    &nbsp;
    <img alt="Stars" src="https://img.shields.io/github/stars/BingyanStudio/LapisCV?style=flat-square&color=2f86d2">
    &nbsp;
    <img alt="Downloads" src="https://img.shields.io/github/downloads/BingyanStudio/LapisCV/total?style=flat-square&color=5e76c3">  
</div><br>

基于 Markdown 格式，易于编辑，所见即所得。风格简洁正式，支持多页，适用于大部分求职 / 求学场景。

### 预览

- 编辑页

<div align="center">
<div>
<img src=".assets/screenshot-obsidian.png" width="90%" />
</div>
</div>

- [PDF样例](https://raw.githubusercontent.com/BingyanStudio/LapisCV/main/.assets/preview.pdf)

<br>
<div align="center">
<img width="80%" alt="Screenshot" src=".assets/preview.png">
</div>

### 安装与使用

#### Typora

1. 下载 [Release](https://github.com/BingyanStudio/LapisCV/releases/latest)，设置 Lapis Cv 作为主题：
   
    1. 在 Typora 菜单中选择 偏好设置 (Preferences) -> 找到外观部分，点击“打开主题文件夹”按钮
    2. 将 lapis-cv.css 和 lapis-cv 文件夹复制到 Typora 的主题文件夹中
    3. 重启 Typora，然后从主题列表中选择 Lapis Cv
    
3. 打开模版文件 [template.md](templates/typora/template.md) 进行内容编辑，文件 - 导出 - PDF 即可导出 PDF 文件。

#### VSCode

1. 下载 [Release](https://github.com/BingyanStudio/LapisCV/releases/latest) 并解压。
2. 在 VSCode 中打开该文件夹，并安装插件 [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf)。
3. 打开模版文件 [template.md](templates/vscode/template.md) 进行内容编辑，右上角点击 Open Preview 图标可进行实时预览。右键选择 Markdown PDF - Export (pdf) 即可导出 PDF 文件。

需要注意，VSCode 中安装的其他插件可能会影响预览显示效果，若预览效果与生成 PDF 中效果不一致，请检查是否有插件影响。

#### Obsidian

下载 [Release](https://github.com/BingyanStudio/LapisCV/releases/latest)，将 `lapis-cv-obsidian` 目录作为 Vault 在 Obsidian 打开，编辑 template 并导出 PDF 文件即可。

### 格式

- 一级标题：姓名块
- 二级标题：栏标题
- 三级标题：栏内子标题
- 引用块：联系方式块
- 分隔线：**分页标记**
  
  支持导出多页简历，可使用分隔线进行手动标记，导出的 PDF 会在分割线处进行一次分页。
- `<img alt="avatar" src="...">`：头像，编辑头像时替换 src 图片路径即可，不带头像可删除该行
> Obsidian 无法识别 html 格式的本地图片插入，因此推荐将图片上传为链接再插入

### 自定义样式

支持自定义样式，便于适配不同体量的单页内容 & 根据喜好调整样式细节。

#### Typora

修改主题文件夹中的 `lapis-cv.css` 并重启 Typora。

部分自定义变量含义如下：

```css
/* Custom Config */

:root {
    --text-size: 10pt;                      // 文本字体大小
    --line-height: 1.8;                     // 文本行高
    --avatar-width: 29mm;                   // 头像宽度

    --text-color: #353a42;                  // 文本颜色，若需打印请改为纯黑
    --primary-color: #4870ac;               // 主题色
    --link-color: #0563c1;                  // 链接颜色
    --shadow-color: #dae3eac9;
    --border-color: #dae3ea;

    --h1-size: 16pt;                        // 一级标题字体大小
    --h2-size: 12pt;                        // 二级标题字体大小
    --h3-size: 10.5pt;                      // 三级标题字体大小

    --text-font: 'SourceHanSansCN';         // 文本字体
    --title-font: 'SourceHanSerifCN';       // 标题字体
    --link-font: 'JetBrainsMono';           // 链接字体
    --code-font: 'JetBrainsMono';           // 代码字体
}

// 打印页边距
@media print {
    @page {
        margin: 12mm 6mm 0 6mm;             // 上边距 左边距 下边距 右边距
    }
}
```

#### VSCode

修改 `lapis-cv.css` 即可。具体样式可参考上述 Typora 部分。

其中页边距需要在 VSCode 设置中修改：

- 直接修改 .vscode/settings.json 文件中的 markdown-pdf.margin 相关项。

- 另外的，还可以通过 GUI 进行修改：

    1. 打开 VSCode 设置，选中 Workspace 标签页。
    2. 搜索 Markdown-pdf › Margin，并修改四边边距。

无需重启 VSCode，重新生成 PDF 即可生效。

#### Obsidian

可在 设置 - 外观 中快速更换主题色与字体，其他样式在 `.obsidian/themes/lapis-cv.css` 修改，具体样式可参考上述 Typora 部分。
