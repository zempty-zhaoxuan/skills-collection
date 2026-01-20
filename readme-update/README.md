# README Update 插件

README 文档自动更新助手，检测插件变更并生成规范的文档。

## 安装

```bash
/plugin install readme-update@skills-collection
```

## 功能列表

### 技能 (Skills)

| 技能名称 | 描述 | 触发方式 |
|---------|------|---------|
| readme-update | README 文档自动更新助手 | `更新 README`、`同步文档` |

## 使用说明

### readme-update 技能

自动检测插件市场变更，生成和更新规范的 README 文档。

**功能特点**：

1. **扫描插件目录** - 遍历所有插件，检测 skills、commands、agents、hooks
2. **收集插件信息** - 从 plugin.json 和各目录提取元数据
3. **更新根目录 README** - 生成插件统计表格和使用说明
4. **更新插件 README** - 为每个插件生成详细的使用文档

**触发方式**：

```
更新 README
同步文档
生成插件统计
更新插件市场文档
```

**输出示例**：

根目录 README 插件统计表格：

| 插件名称 | 描述 | 技能 | 命令 | 代理 | Hooks | 版本 |
|---------|------|------|------|------|-------|------|
| leetcode | LeetCode 算法题解助手 | 1 | 0 | 0 | 0 | 1.0.0 |
| readme-update | README 文档更新助手 | 1 | 0 | 0 | 0 | 1.0.0 |

## 目录结构

```
readme-update/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── readme-update/
│       └── SKILL.md
└── README.md
```
