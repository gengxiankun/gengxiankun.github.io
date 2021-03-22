# 内部变量
> bash 的内部变量会影响 bash 脚本中的行为

## $BASH
用于引用 BASH 实例的全路径名

## $HOME
当前用户的 home 目录

## $IFS
IFS 是内部字段分隔符的缩写

## $OSTYPE
操作系统的类型

## $SECONDS
脚本已经运行的秒数

## $TIMEOUT
如果该变量被指定了一个非零的指，此值会被 bash 的内部命令 read 作为默认的超时秒数

## $UID
当前用户的账号标示码；即使该账户通过 su 命令已经临时获得了另一个账户的权限。
$UID 是一个只读变量，不接受从命令行获脚本的修改。下面来判断当前账户是否为 root ：

```bash
root_uid=0
if [ "$UID" -eq "$root_uid" ]
then
	echo "you are root"
else
	echo "you ain't root"
fi
```
