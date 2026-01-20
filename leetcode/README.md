# LeetCode 插件

LeetCode 算法题解助手插件，提供系统化、多角度的解题指导。

## 安装

```bash
# 本地加载
claude --plugin-dir ./leetcode
```

## 技能列表

| 技能名称 | 描述 |
|---------|------|
| leetcode-solver | LeetCode 算法题解助手 |

## leetcode-solver

### 功能特点

- **题目确认**：自动搜索并确认题目信息，包括难度和标签
- **思路分析**：问题拆解、数据结构选择、算法策略分析
- **多种解法**：提供至少三种不同思路的 Java 解法
- **复杂度对比**：时间和空间复杂度对比表格
- **执行示例**：逐步演示算法执行过程

### 触发方式

- 题号：`第1题`、`LeetCode 1`、`1`
- 题名：`两数之和`、`Two Sum`

### 输出示例

```
【题目】LeetCode 第 1 题：两数之和
【难度】简单
【标签】数组、哈希表

[思路分析...]

[三种解法的 Java 实现...]

[复杂度对比表格...]

[执行示例...]
```

## 目录结构

```
leetcode/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   └── leetcode-solver/
│       └── SKILL.md
└── README.md
```
