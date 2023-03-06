# 补充内容

## 补充：文法的构造方式

### 特征一：语言中的所有句子都只含有单个符号

**例如**：对于字母表$\Sigma=\{a,b,c\}$构造文法使其描述语言：


$$
L=\{a^{2n},b^{2n}\mid n\in\mathbb{N}\}
$$


可构造规则


$$
S\rightarrow A\mid B\mid \varepsilon
$$

分别构造只包含符号$a$的句子和$b$的句子。

然后通过构造$A$和$B$分别为左项的规则：


$$
A\rightarrow aa\mid aaA,\quad B\rightarrow bb\mid bbB,
$$


 

### 特征二：必须是某类符号作为起始符号

**例如**：变量标识符必须以字母开头，并由字母、数字的集合构成

可以构造规则：


$$
S\rightarrow L\mid SL\mid SD
$$


其中，$D$的候选式均为数字，$L$的候选式均为字母。



### 特征三：成对出现的某符号对

**例如**：算术表达式中的括号必须配对，即给定字母表包含"{"和"}"，构造语言


$$
L=\{(^n)^n\mid n\in \mathbb{N}\}
$$


由于成对出现，故若要产生括号，则左右括号必须一同生成，那么可以构造规则：


$$
S\rightarrow (S)\mid\varepsilon
$$