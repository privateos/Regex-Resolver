# Regex-Resolver
基于NFA(不确定有穷自动机)与自底向上语法分析构造的正则表达式解析器

### Regex-Resolver流程构造剖析:

### 基本原理
首先将正则表达式理解为由某些字符串所组成的一种语言的集合, 进而对字符串的组成进行分析,
将其分割成基本的字符串、连接、或、乘积这几种基本的运算组合。
从而得到对于正则表达式本质的基本理解(即由某些特定的字符串及其通过连接、或、幂运算所构成的语言集的集合)。

### 正则表达式的NFA(不确定有穷自动机)
在继上面所得到的对于正则表达式的基本理解之后, 我们发现对于正则表达式的验证流程即从左至右依次验证的流程。
于是我们便可将其视作为一种状态转换的流程，由此我们便可将上面所述的基本运算将其转换为NFA自动机的构建。

对于每一个基本符号(a)构建如下图的自动机:
<div align="space-between">
  <img src="https://github.com/Panda-Hope/panda-hope.github.io/blob/master/gif/regex1.png" width="293" height="109">
</div>
然后对于字符的连接、或、幂运算分别构造如下图所示的自动机:
<div align="space-between">
  <img src="https://github.com/Panda-Hope/panda-hope.github.io/blob/master/gif/regex4.png" width="617" height="157">
  <img src="https://github.com/Panda-Hope/panda-hope.github.io/blob/master/gif/regex2.png" width="658" height="253">
  <img src="https://github.com/Panda-Hope/panda-hope.github.io/blob/master/gif/regex3.png" width="645" height="283">
</div>


