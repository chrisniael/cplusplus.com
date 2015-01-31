函数

# isalnum

\<cctype\>

`int isalnum ( int c );`

#### 检查字符是否是字母数字(alphanumeric)

检查字符 _c_ 是否是一个十进制数字或者是大写或小写字母。

函数返回值是 _true_，那么 [isalpha](isalpha.md) 和 [isdigit](isdigit.md) 也返回 _true_。

注意，字母是什么取决于使用环境。在默认的 "C" 环境中，

