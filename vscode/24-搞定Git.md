# 第二十四天

## 目标

搞定Git

## 任务点

### 显示源码管理界面

- `ctrl + shift + g`

```json
// 打开Git管理
{
  "before": ["<leader>", "g", "g"],
  "commands": ["workbench.view.scm"]
},
```

### git add (暂存更改)

- 命令：git.stage

```json
// git add
{
  "before": ["<leader>", "g", "s"],
  "commands": ["git.stage"]
},
```

### git commit （提交）

- 命令：git.commitStaged

```json
// git commit
{
  "before": ["<leader>", "g", "c"],
  "commands": ["git.git.commit"]
},
```

## git push

- 命令：git.push

```json
// git push
{
  "before": ["<leader>", "g", "p"],
  "commands": [{ "command": "git.push" }]
},
```

### git diff

- 命令：git.timeline.openDiff

```json
// git diff
{
  "before": ["<leader>", "g", "d", "f"],
  "commands": ["git.timeline.openDiff"]
},
```

### 撤销 add

- 命令：git.unstage

```json
// 撤销add
{
  "before": ["<leader>", "g", "u"],
  "commands": ["git.unstage"]
},
```

### 撤销 commit

- 命令：git.undoCommit

```json
// git uncommit
{
  "before": ["<leader>", "g", "u", "c"],
  "commands": ["git.undoCommit"]
},
