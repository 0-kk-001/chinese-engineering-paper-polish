# 中文工科论文润色优化

面向中文工科论文的写作润色技能，根据项目直接生成的论文通常都不能看，必须经过多轮的修改才能勉强可用，经过最近一段时间的改稿与网上总结制作了该skill，由于我的论文是工科，所以该skill可能更适合工科论文写作。

## 可以做什么

- 文章整体逻辑上层层递进，不让每章节或每段内容看起来太割裂。
- 梳理问题、设计、机制和证据之间的关系，突出有依据的研究贡献。
- 消除长句、模糊指代和段落拼接，统一术语、缩写、符号及公式说明。
- 优化摘要、引言、方法、实验和结论，并使图表服务于论证。


## 安装与调用

将本仓库放入 Codex 的技能目录，文件夹名称保持为 chinese-engineering-paper-polish。Windows PowerShell 示例：

~~~powershell
git clone https://github.com/0-kk-001/chinese-engineering-paper-polish.git "$env:USERPROFILE/.codex/skills/chinese-engineering-paper-polish"
~~~

调用示例：

~~~text
使用 $chinese-engineering-paper-polish，依据批注整体优化论文，
~~~

也可以限定范围：

~~~text
使用 $chinese-engineering-paper-polish，只润色以下方法小节，
重点改善段落衔接、符号解释和图文关系，不新增实验结果。
~~~
## 许可证

本项目采用 [MIT 许可证](LICENSE)。
