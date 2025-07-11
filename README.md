# Rime 简体拼音输入法配置

一个专为简体中文用户优化的 Rime 输入法配置，提供简洁高效的输入体验。

## ✨ 特性

### 🎯 简化配置
- **纯简体拼音**：只保留朙月拼音·简化字方案，去除不必要的输入方案
- **智能默认**：默认中文模式、半角符号、中文标点
- **横向布局**：候选词横向排列，符合现代输入习惯

### 🔧 智能输入
- **模糊拼音**：支持平翘舌、前后鼻音、边鼻音等常见模糊音
- **拼写纠错**：内置按键纠错和拼写纠错功能
- **技术词汇**：专门的技术词典，包含编程、算法、数据结构等专业词汇
- **句子学习**：智能学习用户输入习惯，提升输入准确率

### 🎨 视觉体验
- **多种主题**：内置 7 种精美配色方案
- **macOS 原生风格**：完美融入 macOS 系统界面
- **状态提示**：清晰的输入模式切换提示

### ⌨️ 快捷操作
- **Shift 快速切换**：输入拼音时按 Shift 直接输出英文
- **Caps Lock 支持**：Caps Lock 切换中英文模式
- **智能标点**：自动转换中英文标点符号

## 📦 安装

### 前置要求
- macOS 系统
- [Rime 输入法](https://rime.im/) (推荐使用 Squirrel)

### 安装步骤

1. **备份现有配置**（如果有）：
   ```bash
   cp -r ~/Library/Rime ~/Library/Rime.backup
   ```

2. **克隆配置**：
   ```bash
   git clone https://github.com/your-username/rime-config.git ~/Library/Rime
   ```

3. **重新部署**：
   - 在输入法菜单中选择「重新部署」
   - 或使用快捷键 `Control + Option + ~`

## 🎨 主题预览

配置包含 7 种精美主题：

| 主题名称 | 描述 | 适用场景 |
|---------|------|---------|
| **简约灰** | 低调优雅的灰色主题 | 日常使用，护眼 |
| **macOS 原生** | 深色模式原生风格 | macOS 深色模式 |
| **macOS 浅色** | 浅色模式原生风格 | macOS 浅色模式 |
| **北欧风格** | 清新的北欧配色 | 简约爱好者 |
| **温暖橙色** | 温暖的橙色调 | 需要活力时 |
| **薄荷绿** | 清新的薄荷绿 | 护眼需求 |
| **紫色梦幻** | 梦幻的紫色系 | 个性化需求 |

### 切换主题
编辑 `squirrel.custom.yaml` 文件中的 `style/color_scheme` 字段：
```yaml
patch:
  style/color_scheme: minimal_gray  # 更改为你喜欢的主题名称
```

## ⚙️ 配置说明

### 核心配置文件

| 文件 | 功能 |
|------|------|
| `default.custom.yaml` | 全局设置，输入方案列表 |
| `luna_pinyin_simp.custom.yaml` | 简体拼音方案配置 |
| `squirrel.custom.yaml` | 外观主题配置 |
| `grammar.custom.yaml` | 语法模型优化 |

### 词典文件

| 文件 | 内容 |
|------|------|
| `pinyin_simp_tech.dict.yaml` | 技术词汇（274个词条） |
| `luna_pinyin.extended.dict.yaml` | 扩展词库 |

## 🔧 自定义配置

### 修改候选词数量
编辑 `default.custom.yaml`：
```yaml
patch:
  menu:
    page_size: 5  # 修改为你想要的数量
```

### 添加自定义词汇
编辑 `pinyin_simp_tech.dict.yaml`，按格式添加：
```yaml
你的词汇	ni de ci hui
```

### 调整模糊拼音
编辑 `luna_pinyin_simp.custom.yaml` 中的 `fuzzy_pinyin` 部分。

## 📝 技术词汇

配置包含丰富的技术词汇，涵盖：

- **编程语言**：JavaScript, Python, Java, C++, Go, Rust 等
- **数据结构**：数组、链表、栈、队列、哈希表、二叉树等
- **算法**：排序、搜索、动态规划、贪心算法等
- **框架工具**：React, Vue, Spring, Django, Docker 等
- **计算机概念**：API、数据库、网络协议、设计模式等

## 🚀 使用技巧

### 快速切换中英文
- **方法一**：输入拼音时按 `Shift` 直接输出英文
- **方法二**：使用 `Caps Lock` 切换输入模式
- **方法三**：使用 `Control + Space` 切换

### 智能标点
- 输入 `\` 自动转换为顿号 `、`
- 输入 `_` 自动转换为破折号 `——`
- 单双引号自动转换为中文引号

### 模糊拼音示例
- `zhong` 和 `zong` 都能输入「中」
- `ying` 和 `yin` 都能输入「音」
- `lan` 和 `nan` 都能输入「南」

## 🛠️ 故障排除

### 重新部署
如果遇到问题，尝试重新部署：
1. 输入法菜单 → 重新部署
2. 或使用快捷键 `Control + Option + ~`

### 查看日志
日志文件位置：`~/Library/Logs/Squirrel.log`

### 恢复默认
```bash
rm -rf ~/Library/Rime
# 重新安装 Rime 或恢复备份
```

## 📄 许可证

本配置基于 [MIT License](LICENSE) 开源。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 贡献指南
1. Fork 本仓库
2. 创建特性分支
3. 提交更改
4. 发起 Pull Request

## 📞 支持

如有问题，请：
1. 查看 [Issues](https://github.com/your-username/rime-config/issues)
2. 提交新的 Issue
3. 参考 [Rime 官方文档](https://rime.im/docs/)

---

**享受高效的中文输入体验！** 🎉
