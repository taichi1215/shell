# Shell

#!/bin/bash
your_name="qinjx"
greeting="hello, "$your_name" !"
greeting_1="hello, ${your_name:0:3} !"
echo $greeting $greeting_1
echo `expr index "$your_name" q` #输出1

array_name=(
value0
value1
value2
value3
)
echo ${array_name[@]}#获取所有元素 



$# 	传递到脚本的参数个数
$* 	以一个单字符串显示所有向脚本传递的参数。
如"$*"用「"」括起来的情况、以"$1 $2 … $n"的形式输出所有参数。
$$ 	脚本运行的当前进程ID号
$! 	后台运行的最后一个进程的ID号
$@ 	与$*相同，但是使用时加引号，并在引号中返回每个参数。
如"$@"用「"」括起来的情况、以"$1" "$2" … "$n" 的形式输出所有参数。
$- 	显示Shell使用的当前选项，与set命令功能相同。
$? 	显示最后命令的退出状态。0表示没有错误，其他任何值表明有错误。

#用法
echo "执行的文件名：$0";
echo "第一个参数为：$1";
echo "参数个数为：$#";