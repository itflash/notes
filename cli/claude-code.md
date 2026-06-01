---
title: Claude Code
parent: CLI
nav_order: 1
---

# Claude Code

## 常用命令

以宽松权限模式启动 Claude Code：

```bash
claude --dangerously-skip-permissions \
  --permission-mode acceptEdits \
  --allowed-tools "Read,Write,Edit,Bash"
```

### 参数说明

| 参数                               | 说明          |
| -------------------------------- | ----------- |
| `--dangerously-skip-permissions` | 跳过权限提示，直接执行 |
| `--permission-mode acceptEdits`  | 自动接受编辑操作    |
| `--allowed-tools "..."`          | 允许使用的工具列表   |
