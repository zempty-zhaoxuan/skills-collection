# README Update 插件

skills-collection 插件市场文档更新助手，专用于更新 **zempty-zhaoxuan/skills-collection** 仓库的 README 文档。

> **适用范围**：仅用于更新当前仓库（skills-collection）下的 README 文件，不适用于其他项目。

## 安装

```bash
/plugin install readme-update@skills-collection
```

## 功能列表

### 技能 (Skills)

| 技能名称 | 描述 | 触发方式 |
|---------|------|---------|
| plugins-update | skills-collection 插件市场文档更新助手 | `更新插件文档`、`同步 README` |

## 使用说明

### plugins-update 技能

专用于 zempty-zhaoxuan/skills-collection 仓库的文档更新助手。

**功能特点**：

1. **扫描插件目录** - 遍历 skills-collection 中的所有插件，检测 skills、commands、agents、hooks
2. **收集插件信息** - 从 plugin.json 和各目录提取元数据
3. **更新根目录 README** - 生成 `skills-collection/README.md` 的插件统计表格
4. **更新插件 README** - 为 skills-collection 中的每个插件生成详细使用文档

**触发方式**：

```
更新插件文档
同步 README
生成插件统计
更新 skills-collection 文档
```

**输出示例**：

根目录 README 插件统计表格：

| 插件名称 | 描述 | 技能 | 命令 | 代理 | Hooks | 版本 |
|---------|------|------|------|------|-------|------|
| leetcode | LeetCode 算法题解助手 | 1 | 0 | 0 | 0 | 1.0.0 |
| readme-update | 文档更新助手 | 1 | 0 | 0 | 0 | 1.0.0 |

**更新的文件路径**：

- 根目录 README：`skills-collection/README.md`
- 插件 README：`skills-collection/插件名/README.md`

## 目录结构

```
readme-update/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── plugins-update/
│       └── SKILL.md
└── README.md
```
