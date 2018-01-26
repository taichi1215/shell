#shell printf命令
printf  format-string  [arguments...]
#实例


```
#!/bin/bash
# author:菜鸟教程
# url:www.runoob.com
 
printf "%-10s %-8s %-4s\n" 姓名 性别 体重kg  
printf "%-10s %-8s %-4.2f\n" 郭靖 男 66.1234 
printf "%-10s %-8s %-4.2f\n" 杨过 男 48.6543 
printf "%-10s %-8s %-4.2f\n" 郭芙 女 47.9876 
```
#printf的转义序列
序列	说明
\a	警告字符，通常为ASCII的BEL字符
\b	后退
\c	抑制（不显示）输出结果中任何结尾的换行字符（只在%b格式指示符控制下的参数字符串中有效），而且，任何留在参数里的字符、任何接下来的参数以及任何留在格式字符串中的字符，都被忽略
\f	换页（formfeed）
\n 	换行
\r	回车（Carriage return）
\t	水平制表符
\v	垂直制表符
\\	一个字面上的反斜杠字符
\ddd 	表示1到3位数八进制值的字符。仅在格式字符串中有效
\0ddd	表示1到3位的八进制值字符


#Shell test 命令


### 数值测试
参数 	说明
-eq 	等于则为真
-ne 	不等于则为真
-gt 	大于则为真
-ge 	大于等于则为真
-lt 	小于则为真
-le 	小于等于则为真

### 实例演示：

num1=100
num2=100
if test $[num1] -eq $[num2]
then
    echo '两个数相等！'
else
    echo '两个数不相等！'
fi
# 字符串测试
参数 	说明
= 	等于则为真
!= 	不相等则为真
-z 字符串 	字符串的长度为零则为真
-n 字符串 	字符串的长度不为零则为真

###  实例演示：

num1="ru1noob"
num2="runoob"
if test $num1 = $num2
then
    echo '两个字符串相等!'
else
    echo '两个字符串不相等!'
fi
## 文件测试
参数 	说明
-e 文件名 	如果文件存在则为真
-r 文件名 	如果文件存在且可读则为真
-w 文件名 	如果文件存在且可写则为真
-x 文件名 	如果文件存在且可执行则为真
-s 文件名 	如果文件存在且至少有一个字符则为真
-d 文件名 	如果文件存在且为目录则为真
-f 文件名 	如果文件存在且为普通文件则为真
-c 文件名 	如果文件存在且为字符型特殊文件则为真
-b 文件名 	如果文件存在且为块特殊文件则为真

### 实例演示：

cd /bin
if test -e ./bash
then
    echo '文件已存在!'
else
    echo '文件不存在!'
fi

