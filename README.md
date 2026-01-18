# LinDream 插件安装指南

## 📦 插件简介

本插件是用于 LinDream QQ 机器人框架的扩展插件，提供额外的功能和特性。

## 🚀 安装方式

### 方式一：手动安装（推荐）

1. **下载插件**
   - 从插件仓库下载插件的 `.zip` 压缩包

2. **解压插件**
   - 将压缩包解压到 LinDream 项目的 `plugin/` 目录下
   - 确保解压后的文件夹结构正确，通常包含 `main.py` 或 `plugin.json` 文件

   ```
   LinDream/
   ├── plugin/
   │   └── 你的插件名/
   │       ├── main.py          # 插件主文件
   │       ├── requirements.txt # 依赖列表（可选）
   │       └── ...              # 其他插件文件
   ```

3. **重启机器人**
   - 重启 LinDream 机器人，插件将自动加载

## 📋 插件要求

### 必需文件

插件必须包含以下文件之一：

- **Python 插件**：`main.py` - 插件主文件，必须实现以下函数之一：
  - `on_message(websocket, data, bot_id)` - 处理消息
  - `on_command(websocket, data, command, bot_id)` - 处理指令
  - `on_load()` - 插件加载时调用

- **多语言插件**：`plugin.json` - 插件配置文件

### 可选文件

- `requirements.txt` - 插件依赖列表，系统会自动安装
- `README.md` - 插件说明文档
- 其他插件所需的资源文件

## 🔧 插件数据目录

插件的数据会自动存储在 `data/plugin_data/插件名_data/` 目录下，确保数据隔离和管理。

## 📝 插件开发

如需开发自定义插件，请参考：

- [LinDream 完整文档](https://RBfrom.havugu.cn/docs)
- [插件开发指南](https://RBfrom.havugu.cn/docs/plugin-development)

## ⚠️ 注意事项

1. **权限要求**：安装插件需要管理员权限
2. **依赖安装**：插件首次加载时会自动安装依赖，请确保网络连接正常
3. **兼容性**：请确保插件与你的 LinDream 版本兼容
4. **安全性**：只从可信来源下载插件，避免安装恶意插件

## 🆘 常见问题

### Q: 插件加载失败怎么办？
A: 检查插件文件结构是否正确，查看机器人日志获取详细错误信息。

### Q: 如何卸载插件？
A: 使用 `/unload 插件名` 命令卸载插件，或手动删除 `plugin/` 目录下的插件文件夹。

### Q: 插件依赖安装失败？
A: 检查网络连接，或手动安装依赖：`pip install -r plugin/插件名/requirements.txt`

## 📞 支持

如有问题，请访问：
- [LinDream GitHub Issues](https://github.com/DXBbyd/LinDream/issues)
- [插件仓库](https://github.com/DXBbyd/LinDream_plugin)
- [完整文档](https://RBfrom.havugu.cn/docs)