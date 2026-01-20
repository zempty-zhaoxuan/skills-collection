# Skills Collection

个人插件市场，收录和总结好用的 Claude Code 技能插件集合。

## 插件列表

| 插件名称 | 描述 | 技能数量 |
|---------|------|---------|
| [leetcode](./leetcode/) | LeetCode 算法题解助手 | 1 |

## 使用方式

### 添加市场源

```bash
# 通过 GitHub 添加
/plugin marketplace add zempty-zhaoxuan/skills-collection

# 或通过 Git URL 添加
/plugin marketplace add https://github.com/zempty-zhaoxuan/skills-collection.git
```

### 安装插件

```bash
/plugin install leetcode@skills-collection
```

### 本地开发

```bash
# 本地加载单个插件
claude --plugin-dir ./leetcode
```

## 目录结构

```
skills-collection/
├── .claude-plugin/
│   └── marketplace.json
├── README.md
└── leetcode/
    ├── .claude-plugin/
    │   └── plugin.json
    ├── skills/
    │   └── leetcode-solver/
    │       └── SKILL.md
    └── README.md
```

## 贡献

欢迎提交 PR 添加新的插件或改进现有插件。
