# 参数扩展

## 间接参数扩展
`${!parameter}`: 被引用的参数不是 parameters 自身，而是 parameters 的值。

## 大小写修改
- `${parameters^}`: 操作符 `^` 将参数值的第一个字符改为大写
- `${parameters,}`: 操作符 `,` 将参数值的第一个字符改为小写
- `${parameters^^}、${parameters,,}`: 当使用双重模式（`^^`和`,,`）时，参数值的所有字符都将被转换

## 变量名扩展
- `${!prefix*}`: 这种参数扩展将列出以字符串prefix开头的所有变量名

## 字符串移除
- `${parameters#pattern}`: 用于移除从参数值的开头匹配指定模式的最短字符串
- `${parameters%pattern}`: 用于移除从参数值的开头匹配指定模式的最长字符串
- `${parameters##pattern}、${parameters%%pattern}`: 操作符##和%%表示匹配制定模式的最长文本

## 字符换搜索与替换
- `${parameters/pattern/string}`: 操作符 `/` 表示只替换一个匹配的字符
- `${parameters//pattern/string}`: 操作符 `//` 表示替换所有匹配的字符
- `${parameters/pattern}、${parameters//pattern}`: 如果没有指定替换字符的 string ，那么匹配的内容将被替换为空字符，即被删除。

## 求字符串的长度
`${# parameters}`

## 子字符串扩展
`${parameters:offset}、${parameters:offset:length}`: 从指定位置开始截取指定长度的字符串，如省略lengh，将截取到末尾

## 使用默认值
- `${parameters:-word}`: 如果参数 parameters 未定义，或者为 null 时，这种模式将会扩展 word
- `${parameters-word}`: 这种模式只有参数 parameters 未定义时才被 word 扩展

## 指定默认值
- `${parameters:=word}、${parameters=word}`: 这种模式与使用默认值类似，区别在于不仅扩展 word ，还将 word 的值赋给 parameters

## 使用替代值
- `${parameters:+word}、${parameters+word}`: 如果参数 parameters 是未定义的，或其值为空时，这种模式将不扩展任何内容。
