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

