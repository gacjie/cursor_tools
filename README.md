# Cursor Tools

一个基于 PySide6 (Qt for Python) 的桌面应用，用于管理 Cursor IDE 的账号、机器码与配置。它支持从 Cursor 在线服务模拟登录流程获取令牌、在本地数据库管理多个账号、一键切换账号、备份/还原 Cursor 配置文件，以及常用的运维工具（重置机器码、初始化 Cursor 数据等）。

> 适用平台：Windows 


## 功能特性
- 仪表盘
  - 可视化显示当前 Cursor 的账号与机器码信息（邮箱、套餐、Token 状态、各类 Machine/Telemetry/SQM ID 等）
- 账号管理
  - 本地 SQLite 数据库存储多个账号（添加/编辑/删除/导入/导出）
  - 一键切换账号（自动写入 Cursor 的 state.vscdb、storage.json 与 machineid 文件）
- 获取令牌
  - 支持基于 PKCE 的三步流程：生成授权链接 → 轮询交换令牌 → 保存账号到本地数据库
- 配置备份
  - 备份/还原以下文件：
    - ~/.cursor/mcp.json（或 Windows 下 %USERPROFILE%/.cursor/mcp.json）
    - Cursor/User/settings.json
  - 自动维护备份索引，支持按名称/说明管理与显示
- 实用工具
  - 重置所有机器码（保持 machineId 与 serviceMachineId 一致）
  - 初始化 Cursor（危险操作：清空 Cursor 与 .cursor 目录）
- 主题与样式
  - 轻/暗两套主题，统一风格（标题栏、侧边栏、卡片与表格等）


## 截图
（可选：自行添加）

## 使用指南
### 仪表盘
- 展示当前 Cursor 的账号邮箱、套餐、Token 状态与机器码（多处做了安全截断显示与 tooltip）。
- 若系统未安装 Cursor 会提示“未安装”。

### 账号管理
- 通过“添加账号”或“编辑账号”对话框维护本地数据库账号。
- 必填字段：邮箱 / Access Token / Refresh Token。
- Machine ID 与 Service Machine ID 必须相同：
  - 对话框提供“一键生成”与“同步”按钮，保存前会自动校正二者一致。
- 表格支持导入/导出 JSON；“切换账号”会将账号与机器码写入 Cursor 所需位置，重启 Cursor 生效。

### 获取令牌
- 第一步生成授权链接（自动复制到剪贴板，可一键在浏览器打开）。
- 第二步后台轮询交换令牌（带精致的 Loading UI）。
- 第三步展示邮箱/套餐/令牌关键信息，确认后保存到本地数据库。

### 配置备份
- 备份 .cursor/mcp.json 与 Cursor/User/settings.json 到应用数据目录的 config_backups 下，并维护索引。
- 可视化列表展示备份名称、包含项与创建日期，支持还原/删除。
- 还原前会备份当前文件至 .bak，提示重启 Cursor 生效。

### 实用工具
- 重置所有机器码：
  - 生成一套新的 machineId / telemetry.devDeviceId / telemetry.macMachineId / telemetry.machineId / telemetry.sqmId
  - 保证 serviceMachineId 与 machineId 一致并写回 state.vscdb
  - 附带详细执行日志与结果统计
- 初始化 Cursor（危险操作）：
  - 删除 Cursor 与 .cursor 目录（跨平台处理），请务必先做好备份

## 常见问题（FAQ）

- Q: 切换账号后为什么要重启 Cursor？
  - A: Cursor 进程通常会缓存状态，需重启以重新读取 state.vscdb、storage.json 与 machineid。

- Q: 初始化 Cursor 提示失败？
  - A: 确认 Cursor 已完全退出；Windows 下注意文件被占用；必要时提升权限或重试。

- Q: Token 获取失败/超时？
  - A: 检查网络、代理与防火墙；稍后重试。获取订阅信息失败不会阻止保存账号。

## 致谢
- PySide6, Qt for Python
- Requests
- Cursor IDE 团队与社区贡献者
