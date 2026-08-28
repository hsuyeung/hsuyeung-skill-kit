# hsuyeung-skill-kit

一组可以独立安装、按需使用的 Agent Skills。

## Skills

| Skill | 用途 | 适合场景 |
| --- | --- | --- |
| [**ELI0**](./communication/eli0/) | **Explain Like I Have Zero Context.** 让 AI 面向“有能力但没有前置上下文”的读者解释内容，补齐必要的背景、因果和关键步骤，同时保留技术细节与限制条件。 | 技术解释、方案 Review、README、事故复盘、复杂内容重写 |
| [**Code Comments**](./coding/code-comments/) | 改善 AI 编写和 Review 代码注释的方式：少写复述代码的注释，多保留原因、约束、契约、风险和其他代码本身难以表达的信息。 | 写代码、Review diff、重构旧注释、Docstring / XML Doc / Javadoc / TODO |

## 安装

### 手动安装

打开需要的 Skill 目录，将整个 Skill 文件夹复制到你所使用 AI 工具的 Skills 目录中即可。

例如安装 ELI0，只需要复制 `communication/eli0/` 这个目录。

### 让 AI 助手帮你安装

如果你的 AI 助手可以访问 GitHub 和本地文件，可以直接告诉它：

```text
请从 https://github.com/hsuyeung/hsuyeung-skill-kit 安装 ELI0。
只安装这个 Skill，并放到你当前环境正确的 Agent Skills 目录中。
```

安装其他 Skill 时，把 `ELI0` 换成对应名称即可。
