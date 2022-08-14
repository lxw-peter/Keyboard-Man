# 第二十六天

## 目标

掌握常用 `snippets`

## 任务点

### 插件

- `Javascript(ES6) code snippets`
- `Vue 3 Snippets`
- `Vue VSCode Snippets`

### 常用

- `imp` - `import {  } from "module";`
- `imd` - `import {} from 'module';`
- `fn` - `function name(params) {}`
- `log` - `console.log();`
- `anfn` - `(params) => {};`
- `iife` - `;(function(){})()`

### 技巧

- Tab 键可以切换位置
- 提示消失时使用如下快捷键激活提示
  - `command + i`
  - `Ctrl + space`

### 自定义 `Snippets`

#### 文档参考

- [Snippets in Visual Studio Code](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
- [snippet generator](https://snippet-generator.app/)

#### 知识点

- tab 位置
- 默认值
- 多选
- 变量

```json
{
  // Place your snippets for vue here. Each snippet is defined under a snippet name and has a prefix, body and
  // description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
  // $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the
  // same ids are connected.
  // Example:
  // "Print to console": {
  //  "prefix": "log",
  //  "body": [
  //   "console.log('$1');",
  //   "$2"
  //  ],
  //  "description": "Log output to console"
  // }
  "vue 3 setup": {
    "prefix": "v3s",
    "body": [
      "<template>",
      "  <div>",
      "     $1",
      "  </div>",
      "</template>",
      "",
      "<script setup>",
      "import { $2 } from 'vue';",
      "$3",
      "</script>"
    ],
    "description": "vue 3 setup"
  }
}

```
