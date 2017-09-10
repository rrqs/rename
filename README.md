# rename

## 文件批量重命名工具

最初的想法来自长到令人厌烦的的电视剧名字（大多数下载网站会在电视剧文件名前全部加上网站名网址之类的，导致后面的集数号很难看到）。刚开始用python写了个小脚本，但用起来很不方便，甚至有一次因为写错了代码导致集数完全混乱，因此产生了写一个GUI批量重命名工具的想法。

### 程序中所有选项全部通过正则表达式处理，增强通用性。

进入程序按F1打开帮助窗口。

### 帮助

1.点击Path按钮选择文件夹

2.“筛选正则表达式”中输入正则表达式，则文件夹下不包含符合此正则表达式部分的文件将被筛除。
3.勾选以使用/取消关键词。启用后，对应关键词下方三个输入框将被启用，分别输入三个正则表达式。系统将会在文件名中查找是否有符合以下要求的字符串：a.关键词符合第二个框表达式；b.关键词前面符合第一个框表达式；c.关键词后面符合第三个框表达式。匹配出的关键词即为第二个框匹配出的字符串。如果没有找到，则筛除此文件，共三个筛选器。
4.重命名框输入重命名规则：

```
"\"为转义字符标志，转义字符有
"\a"、"\A"：关键词正则表达式A匹配出的字符串
"\b"、"\B"：关键词正则表达式B匹配出的字符串
"\c"、"\C"：关键词正则表达式C匹配出的字符串
"\n"、"\N"：计数模式序列
```

5.技术模式：勾选计数模式启用计数模式。技术模式下方为计数起点。启用后，重命名中可以使用"\n"或"\N"给文件从技术起点依次计数，文件中的"\n"或"\N"将被替换为从技术起点开始，增量为1的序列，计数起点可为负值。
6.右侧为预览框，显示格式为"原文件名  -->  重命名文件名"。当重命名名称间有冲突时，"重命名文件名"为红色。当当重命名名称与未参与重命名文件名冲突时，"  -->  重命名文件名"为红色。
7.当可以正常重命名时，预览窗口没有红色，重命名按钮可用，点击即可。







