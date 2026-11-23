# 中文工科论文润色优化

面向中文工科论文的 Codex 技能，围绕研究问题、方法贡献与实验结果梳理论文主线，改善段落衔接、技术解释和图文配合。支持全文优化、逐段润色与依据修改意见进行修订，强调保留原始数据、准确表达结论和保护稿件隐私。

## 可以做什么

- 梳理问题、设计、机制和证据之间的关系，突出有依据的研究贡献。
- 消除长句、模糊指代和段落拼接，统一术语、缩写、符号及公式说明。
- 优化摘要、引言、方法、实验和结论，并使图表服务于论证。
- 依据导师或审稿人的修改意见逐项修订，并按要求标记实际改动。

## 安装与调用

将本仓库放入 Codex 的技能目录，文件夹名称保持为 chinese-engineering-paper-polish。Windows PowerShell 示例：

~~~powershell
git clone https://github.com/0-kk-001/chinese-engineering-paper-polish.git "$env:USERPROFILE/.codex/skills/chinese-engineering-paper-polish"
~~~

调用示例：

~~~text
使用 $chinese-engineering-paper-polish，整体润色论文，
保留原始数据，修改处标红，并简述关键改动。
~~~

也可以限定范围：

~~~text
使用 $chinese-engineering-paper-polish，只润色以下方法小节，
重点改善段落衔接、符号解释和图文关系，不新增实验结果。
~~~

## 内容与隐私

技能仅包含通用编辑方法、章节与图表指南及八类改写模式，不包含私人论文、原始修改意见、实验数据或本机路径。当前稿件与修改稿应保存在任务输出目录，不写回技能及其分发文件。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。
