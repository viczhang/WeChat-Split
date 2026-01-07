# 🎉 WeChat-Split - Run Multiple WeChat Accounts on Mac 


这是一个 macOS 微信多开脚本，用于在 macOS 系统上创建多个微信实例，让用户可以同时登录多个微信账号。

  主要功能

   1. 创建多个微信分身：支持创建 2-10 个微信实例（原版 + 分身）
   2. 自动修改 Bundle Identifier：为每个分身分配唯一的标识符
   3. 移除隔离属性：解决应用图标被禁用（显示问号）的问题
   4. 重新签名应用：确保应用可以正常运行
   5. 数据安全保护：删除应用不会丢失聊天数据，重新创建后数据会自动关联

  使用方法

   1 sudo bash wechat_multi_open_v3.sh [数量]

  示例：
   - sudo bash wechat_multi_open_v3.sh - 默认创建 2 个微信（原版 + 1 个分身）
   - sudo bash wechat_multi_open_v3.sh 3 - 创建 3 个微信（原版 + 2 个分身）

  工作流程

   1. 检查 root 权限和微信是否已安装
   2. 检查现有数据文件夹（避免数据丢失）
   3. 删除旧的微信分身应用（保留数据）
   4. 逐个创建新的微信分身：
      - 复制原版应用
      - 移除隔离属性
      - 修改 Bundle Identifier
      - 重新签名
      - 启动应用
   5. 显示创建结果和数据信息

  数据存储

  每个微信分身的数据独立存储在：
   1 ~/Library/Containers/com.tencent.xinWeChat2/
   2 ~/Library/Containers/com.tencent.xinWeChat3/
   3 ...

  注意事项

✦  - 需要 sudo 权限执行
   - 微信升级后需要重新运行脚本
   - 建议重启电脑以确保双击应用能正确打开对应的实例


## ⚙️ System Requirements
- **Operating System**: macOS 10.12 or later
- **Processor**: Intel or Apple Silicon
- **Memory**: At least 4 GB of RAM 
- **Disk Space**: Minimum of 200 MB available space

## 👩‍💻 Troubleshooting
- **Installation Issues**: If you encounter problems during the installation, make sure your macOS is updated. Older systems may not support the app.
- **Performance Issues**: If the app runs slow, ensure you are not running too many other applications simultaneously, as having multiple instances of WeChat can consume more memory.

## 🛠️ Support
If you run into any issues or have questions, please open an issue on the GitHub repository. The community is here to help you.

Thank you for choosing WeChat-Split! Have a great time managing your WeChat accounts.
