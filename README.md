# 中文工科论文润色优化

面向中文工科论文的 Codex 技能，将导师或审稿批注转化为具体修改，围绕研究问题、方法贡献与实验结果梳理论文主线，改善段落衔接、技术解释和图文配合。支持全文优化、逐段润色与 Word 批注提取，强调保留原始数据、准确表达结论和保护稿件隐私。

## 可以做什么

- 梳理问题、设计、机制和证据之间的关系，突出有依据的研究贡献。
- 消除长句、模糊指代和段落拼接，统一术语、缩写、符号及公式说明。
- 优化摘要、引言、方法、实验和结论，并使图表服务于论证。
- 提取 DOCX 批注及对应原文，逐条记录修订状态；配合文档编辑工具标记修改。

## 安装与调用

将本仓库放入 Codex 的技能目录，文件夹名称保持为 chinese-engineering-paper-polish。Windows PowerShell 示例：

~~~powershell
git clone https://github.com/0-kk-001/chinese-engineering-paper-polish.git "$env:USERPROFILE/.codex/skills/chinese-engineering-paper-polish"
~~~

调用示例：

~~~text
使用 $chinese-engineering-paper-polish，依据批注整体优化论文，
保留原始数据，修改处标红，并附逐条批注处理状态。
~~~

也可以限定范围：

~~~text
使用 $chinese-engineering-paper-polish，只润色以下方法小节，
重点改善段落衔接、符号解释和图文关系，不新增实验结果。
~~~

## 提取 Word 批注

提取脚本仅使用 Python 3 标准库，直接读取 DOCX 中的批注和正文锚点，不修改输入文件：

~~~text
python -X utf8 scripts/extract_docx_comments.py "稿件.docx" --out "output/comments.json" --text-out "output/comments.txt"
~~~

输出包含批注原文、对应文字、上下文、章节、作者、时间及可获得的解决状态。段落序号是 XML 顺序，不是 Word 页码；数学排版需要回看原稿。脚本负责提取，实际改写和 Word 修改标记由技能配合文档工具完成。

## 内容与隐私

技能仅包含通用编辑方法、章节与图表指南、八类改写模式及批注提取工具，不包含私人论文、原始批注、实验数据或本机路径。当前稿件与提取结果应保存在任务输出目录，不写回技能及其分发文件；示例使用的 output/ 已加入忽略规则。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。
