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
