# Cursor Tools - Cursor IDE 账号管理工具

<div align="center">
  <img src="app/resources/icons/app_logo.svg" width="128" height="128" alt="Cursor Tools Logo">
  
  **一款专为 Cursor IDE 打造的账号和配置管理工具**
  
  [![Version](https://img.shields.io/badge/版本-v1.0.0-blue)](https://github.com/gacjie)
  [![Platform](https://img.shields.io/badge/平台-Windows%20|%20macOS%20|%20Linux-green)](https://github.com/gacjie)
  [![QQ Group](https://img.shields.io/badge/QQ群-866292271-red)](https://qm.qq.com/cgi-bin/qm/qr?k=866292271)
</div>

---

## 🚀 功能特点

### 📊 仪表盘
- **实时监控**：查看当前 Cursor IDE 中的账号状态
- **信息展示**：显示邮箱、套餐类型、访问令牌等关键信息
- **一键保存**：快速将当前账号信息保存到本地数据库
- **数据刷新**：实时同步 Cursor IDE 的最新状态

### 👥 账号管理
- **多账号支持**：管理多个 Cursor 账号，方便切换使用
- **账号切换**：一键切换不同的 Cursor 账号（需重启 Cursor IDE 生效）
- **信息编辑**：修改账号备注、更新令牌信息
- **安全存储**：所有账号信息加密存储在本地数据库

### 🔑 令牌管理
- **获取令牌**：快速获取 Access Token 和 Refresh Token
- **令牌刷新**：支持使用 Refresh Token 刷新访问令牌
- **有效期管理**：查看令牌状态和有效期

### 🛠️ 实用工具
- **机器码管理**：生成和管理各类机器识别码
  - Machine ID
  - Mac Machine ID
  - Dev Device ID
  - SQM ID
- **配置重置**：清理和重置 Cursor 配置
- **缓存清理**：清理 Cursor 缓存文件

### 💾 配置备份
- **一键备份**：备份 Cursor 的所有配置和设置
- **快速恢复**：从备份文件恢复配置
- **多版本管理**：支持多个备份版本管理
- **跨设备迁移**：轻松在不同设备间迁移配置

## 💻 系统要求

- **操作系统**：Windows 10/11、macOS 10.15+、Linux (Ubuntu 20.04+)
- **Cursor IDE**：需要已安装 Cursor IDE
- **运行环境**：无需额外安装任何依赖

## 📦 安装使用

### Windows 用户
1. 下载 `CursorTools_v1.0.0_Windows.exe`
2. 双击运行即可，无需安装

### macOS 用户
1. 下载 `CursorTools_v1.0.0_macOS.dmg`
2. 打开 DMG 文件，将应用拖入 Applications 文件夹
3. 首次运行可能需要在系统偏好设置中允许运行

### Linux 用户
1. 下载 `CursorTools_v1.0.0_Linux.AppImage`
2. 添加执行权限：`chmod +x CursorTools_v1.0.0_Linux.AppImage`
3. 双击或终端运行

## 🎯 使用指南

### 首次使用
1. 启动 Cursor Tools
2. 软件会自动检测并读取当前 Cursor IDE 的账号信息
3. 在仪表盘查看当前账号状态

### 账号切换
1. 进入「账号管理」页面
2. 点击「添加账号」输入账号信息
3. 选择要切换的账号，点击「切换账号」
4. 重启 Cursor IDE 使更改生效

### 备份配置
1. 进入「配置备份」页面
2. 点击「创建备份」保存当前配置
3. 需要恢复时选择备份文件，点击「恢复配置」

## 🌓 界面主题

支持亮色和暗色两种主题，点击标题栏的主题切换按钮即可切换。

## 📝 注意事项

- ⚠️ 切换账号后需要**重启 Cursor IDE** 才能生效
- ⚠️ 请勿在 Cursor IDE 运行时进行配置恢复操作
- ⚠️ 建议定期备份重要的配置信息
- ⚠️ 所有数据均存储在本地，请妥善保管

## 🔒 数据安全

- 所有账号信息仅存储在本地计算机
- 不会上传任何数据到云端
- 支持数据加密存储（可选）

## 📁 数据存储位置

### Windows
- 应用数据：`%APPDATA%\CursorTools\`
- Cursor 数据：`%APPDATA%\Cursor\` 和 `%USERPROFILE%\.cursor\`

### macOS
- 应用数据：`~/.cursortools/`
- Cursor 数据：`~/.cursor/`

### Linux
- 应用数据：`~/.cursortools/`
- Cursor 数据：`~/.cursor/`

## 🆘 常见问题

### Q: 切换账号后 Cursor IDE 没有变化？
A: 请确保已经完全关闭并重启 Cursor IDE。

### Q: 无法检测到 Cursor IDE？
A: 请确保 Cursor IDE 已正确安装在默认位置。

### Q: Windows 提示软件来源不明？
A: 这是 Windows 的安全提示，点击「更多信息」→「仍要运行」即可。

### Q: macOS 提示无法打开应用？
A: 在系统偏好设置 → 安全性与隐私中允许运行此应用。

## 🤝 联系与支持

- **作者**：GacJie
- **官网**：[www.wepool.vip](https://www.wepool.vip)
- **GitHub**：[github.com/gacjie](https://github.com/gacjie)
- **QQ交流群**：866292271

## 📄 版权信息

Copyright ©2025-2029 GacJie. All rights reserved.

---

<div align="center">
  <b>如果这个工具对您有帮助，请给个 ⭐ Star 支持一下！</b>
</div>