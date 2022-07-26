# 第十八天

## 目标

vim 调用 vscode 的命令

## 任务点

### `commands 字段` 

```json
[
  // 格式化代码
  {
    "before": ["<Leader>", "f", "d"],
    "commands": ["editor.action.formatDocument"]
    
  },
  // 重命名
  {
    "before": ["<Leader>", "r", "n"],
    "commands": ["editor.action.rename"]
  },
  // 折叠
  {
    "before": ["<Leader>", "["],
    "commands": [
      {
        "command": "editor.fold",
      },
      {
        "command": "vim.remap",
        "args": {
          "after": ["$", "%"]
        }
      }
    ]
  }
]
```


## 功能点

### 格式化文档

- vscode： `shift + alt + f`
- vim: `<Leader> + f + d`

## 重命名

- vscode: `f2`
- vim: `<Leader> + f + d`

### 折叠代码

- vscode:`alt + cmd + [`
- vim: `<leader> + [`

## 技巧

- vscode 里面的快捷键配置里可以通过查询关键词(如 `format`, `rename` ）找到对应命令并获取其`ID`
- 然后在 `setting.json` 的 `vim.normalModeKeyBindingsNonRecursive`里 `commands` 填写命令`ID`
- 如果遇到报错的情况，那可能是配置写法的问题，可以通过拷贝命令 `json` 命令查看
