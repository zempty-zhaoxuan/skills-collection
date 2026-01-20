# Skills Collection

个人插件市场，收录和总结好用的 Claude Code 技能插件集合。

## 插件列表

| 插件名称 | 描述 | 技能数量 |
|---------|------|---------|
| [leetcode](./leetcode/) | LeetCode 算法题解助手 | 1 |

## 使用方式

```bash
# 本地加载插件
claude --plugin-dir ./leetcode

# 或通过插件市场安装
/plugin install leetcode@your-marketplace
```

## 目录结构

```
skills-collection/
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
