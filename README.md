# vs-code

`vs-code` 是一个使用 Visual Studio Code 官方脚手架生成的颜色主题扩展。

## 项目结构

- `package.json`：扩展清单，声明主题入口
- `themes/warm-paper-color-theme.json`：主题颜色与语法高亮规则
- `.vscode/launch.json`：本地调试配置
- `vsc-extension-quickstart.md`：官方生成的扩展快速说明

## 本地开发

1. 用 Visual Studio Code 打开当前目录。
2. 按 `F5` 启动 `Extension Development Host`。
3. 在新窗口中按 `Ctrl + K`，再按 `Ctrl + T`。
4. 选择 `Warm Paper` 主题进行预览。

## 主题文件说明

主题核心文件是 `themes/warm-paper-color-theme.json`，主要包含两部分：

- `colors`：控制 VS Code 界面颜色，例如 `editor.background`、`editor.foreground`、`activityBar.background`
- `tokenColors`：控制语法高亮颜色，例如 `comment`、`keyword`、`string`、`function`、`variable`

## 开发建议

- 优先调整这几类颜色：`editor.background`、`editor.foreground`、`comment`、`keyword`、`string`、`function`、`variable`
- 使用 `Developer: Inspect Editor Tokens and Scopes` 查看当前代码的 token scope
- 修改 `themes/warm-paper-color-theme.json` 后，开发宿主窗口会自动应用变更

## 发布

如果后续需要发布到 Marketplace：

1. 安装 `vsce`
2. 执行 `vsce login <publisher-name>`
3. 执行 `vsce publish`

发布前建议先补充：

- `publisher`
- 扩展图标
- 更完整的 Marketplace 描述
