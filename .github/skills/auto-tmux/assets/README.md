# auto-tmux assets

本目录预期只保存指向仓库内外部 submodule 的软链接入口，不保存上游源码副本。当前仓库中的两个入口实际都是 0 字节普通文件（Git mode `100644`），不是软链接；表中为预期目标，不能通过这些占位路径访问上游。修复须追加可追溯来源修订并保留原状态，详见[法器登记](../../../metadata/faqi.json)中 `.github/skills/auto-tmux` 的待办边界。

| 入口 | 预期目标 | 当前状态 | 用途 |
|:---|:---|:---|:---|
| `oh-my-tmux` | `../../../tools/external/.tmux` | 0 字节普通文件，不是软链接 | gpakosz/oh-my-tmux 配置参考 |
| `tmux-src` | `../../../tools/external/tmux` | 0 字节普通文件，不是软链接 | tmux 上游源码参考 |

初始化或更新 submodule（只准备目标仓库，不会把占位文件转换成软链接）：

```bash
git submodule update --init --recursive
```
