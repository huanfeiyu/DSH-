# DeepSeekHarness Plugin Tool v2.6
English version Windows batch script for DeepSeekHarness plugin management. Plugins are sourced from Awesome DeepSeek Harness Plugin.
This release contains raw BAT script and Windows EXE converted from BAT.

## ✨ Changelog
> v2.6 Updates:
> ✅ Added final command preview, console prints the command to be executed for easy verification and debugging
> ✅ Auto conversion logic in remove plugin module: paste `add` install command, script automatically replaces `add` with `remove` for uninstallation
> ✅ Capture npx return code to distinguish success / failure status
> ✅ Compatible with 3 input formats, original valid `remove` commands will not be affected by conversion logic

## 🧰 Full Features
1. Start DeepSeekHarness Web service
2. Check local DeepSeekHarness version number
3. Install DeepSeekHarness plugins
4. Uninstall DeepSeekHarness plugins (Highlight: paste install command and auto convert to uninstall instruction)
5. List all installed plugins

## 📌 Supported input formats (Remove page)
- Format A: Package name only `@smalltailqwq/dsh-client-ui-skin-maid-atelier`
- Format B: plugin subcommand `plugin --profile web remove package`
- Format C: Full DeepSeekHarness command `deepseekharness plugin --profile web add package` (auto convert `add` → `remove`)

## 📋 Prerequisites
- Windows operating system
- Node.js installed (includes npx)
- Initialized DeepSeekHarness project locally
- Run the script inside your DeepSeekHarness project folder

## ❗ Behavior Notes
When attempting to remove a non-existent plugin:
The script will still construct and send the `remove` instruction to DeepSeekHarness. DeepSeekHarness will judge that the plugin does not exist and return a non-zero return code, the script will show `Failed to remove plugin`.
It is recommended to use the "List Installed Plugins" function to verify plugin existence before removal.

> Plugin source: Awesome DeepSeek Harness Plugin

## 📎 Assets
- DeepSeekHarnessPluginTool.bat
- DeepSeekHarnessPluginTool.exe
# DeepSeekHarness Plugin Tool v2.6
这是面向 DeepSeekHarness 的 Windows CMD 批处理管理工具，免去反复手动输入长命令的麻烦。
插件源来自 Awesome DeepSeek Harness Plugin。

## ✨ 更新说明
> v2.6 更新：
> ✅ 新增执行命令预览，控制台输出【最终执行命令】，方便核对脚本转换结果
> ✅ 删除模块增加自动转换逻辑：粘贴 add 安装命令，自动替换为 remove 卸载命令
> ✅ 捕获 npx 命令返回码，自动区分操作成功/失败状态
> ✅ 兼容三种输入格式，原本正常的 remove 命令不会受到转换逻辑影响

## 🧰 全部功能
1. 启动 DeepSeekHarness Web 服务
2. 查询本地 DeepSeekHarness 版本号
3. 安装 DeepSeekHarness 插件
4. 卸载 DeepSeekHarness 插件（特色功能：可直接粘贴安装命令自动转换为卸载指令）
5. 查看当前已安装插件列表

## 📌 删除页面支持三种输入格式
- 格式A：纯包名 `@smalltailqwq/dsh-client-ui-skin-maid-atelier`
- 格式B：plugin子命令 `plugin --profile web remove 包名`
- 格式C：完整DeepSeekHarness命令 `deepseekharness plugin --profile web add 包名`（自动转换 add → remove）

## 📋 使用前提
- Windows 系统
- 已安装 Node.js（自带 npx）
- 本地已初始化好 DeepSeekHarness 项目
- 在 DeepSeekHarness 项目文件夹内运行脚本

## ❗ 行为说明
当尝试删除不存在的插件时：
脚本仍然会正常构造并向 DeepSeekHarness 发送 remove 指令；由 DeepSeekHarness 判断插件不存在并返回非0错误码，脚本提示【删除失败】。
建议删除前使用「列出插件」功能确认插件存在。

> 插件来源：Awesome DeepSeek Harness Plugin
>蓝奏云 https://wwaqb.lanzouu.com/ih1ij4alx9gj
密码:123
