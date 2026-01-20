---
name: plugins-update
description: skills-collection 插件市场文档更新助手。专用于更新 zempty-zhaoxuan/skills-collection 仓库的 README 文档。当用户需要同步插件信息、生成插件统计表格、更新文档时触发。
---

# Plugins Update

专用于 **zempty-zhaoxuan/skills-collection** 插件市场的文档更新助手。

> **适用范围**：仅用于更新当前仓库（skills-collection）下的 README 文件，不适用于其他项目。

## 工作流程

### 1. 扫描插件目录

遍历 skills-collection 仓库根目录，检测所有插件：

```
skills-collection/
├── .claude-plugin/marketplace.json  # 市场配置
└── */                               # 各插件目录
    ├── .claude-plugin/plugin.json   # 插件配置
    ├── skills/                      # 技能目录
    ├── commands/                    # 命令目录
    ├── agents/                      # 子代理目录
    └── hooks/                       # Hooks 目录
```

### 2. 收集插件信息

对每个插件提取以下信息：

| 信息项 | 来源 | 说明 |
|-------|------|------|
| 插件名称 | plugin.json → name | 插件标识符 |
| 插件描述 | plugin.json → description | 功能简介 |
| 版本号 | plugin.json → version | 当前版本 |
| 技能列表 | skills/*/SKILL.md | 统计技能数量和名称 |
| 命令列表 | commands/*.md | 统计命令数量和名称 |
| 子代理列表 | agents/*/agent.md | 统计代理数量和名称 |
| Hooks | hooks/hooks.json | 统计 Hook 配置 |

### 3. 更新根目录 README

更新 `skills-collection/README.md`，生成：

**插件统计表格**：

```markdown
## 插件列表

| 插件名称 | 描述 | 技能 | 命令 | 代理 | Hooks | 版本 |
|---------|------|------|------|------|-------|------|
| [leetcode](./leetcode/) | LeetCode 算法题解助手 | 1 | 0 | 0 | 0 | 1.0.0 |
| [readme-update](./readme-update/) | 文档更新助手 | 1 | 0 | 0 | 0 | 1.0.0 |
```

**使用说明**：
- 添加市场源：`/plugin marketplace add zempty-zhaoxuan/skills-collection`
- 安装插件：`/plugin install 插件名@skills-collection`

**目录结构**：
- 完整的仓库目录树

### 4. 更新插件 README

为 skills-collection 中的每个插件更新 README.md：

**基本信息**：

```markdown
# 插件名称

插件描述

## 安装

/plugin install 插件名@skills-collection

## 功能列表

### 技能 (Skills)

| 技能名称 | 描述 | 触发方式 |
|---------|------|---------|
| skill-name | 描述... | 关键词/命令 |
```

**详细使用说明**：
- 每个技能的用法和示例
- 输入输出说明
- 注意事项

## 输出规范

### 文件路径
- 根目录 README：`skills-collection/README.md`
- 插件 README：`skills-collection/插件名/README.md`

### Markdown 格式
- UTF-8 编码，LF 换行符
- GitHub Flavored Markdown
- 表格对齐、代码块标注语言

### 更新策略
- 保留用户自定义内容
- 仅更新自动生成的统计部分
- 新增插件自动追加到列表

## 触发方式

- `更新插件文档`
- `同步 README`
- `生成插件统计`
- `更新 skills-collection 文档`
