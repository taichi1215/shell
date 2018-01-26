#if else
if condition
then
    command1 
    command2
    ...
    commandN 
fi

 # for 循环

与其他编程语言类似，Shell支持for循环。

for循环一般格式为：

for var in item1 item2 ... itemN
do
    command1
    command2
    ...
    commandN
done

写成一行：

for var in item1 item2 ... itemN; do command1; command2… done;
## 实例
for loop in 1 2 3 4 5
do
    echo "The value is: $loop"
done
#while


```
#!/bin/sh
int=1
while(( $int<=5 ))
do
    echo $int
    let "int++"
done
```

