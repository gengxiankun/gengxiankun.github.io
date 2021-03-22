# 数组变量

## 间接声明一个数组变量
 `ARRAYNAME[INDEX]=value`

## 数组变量可以使用复用赋值格式
 `ARRAYNAME=(value1 value2 ...)`

## 若要引用数组中的某一项内容，必须使用或括号{}
 `echo ${ARRAYNAME[0]}`

## 消除一个数组或数组的成员变量
 `unset ARRAYNAME[2]`

## 数组追加赋值
 `a=(${a[@]} 'c')`
