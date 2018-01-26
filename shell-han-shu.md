#shell函数


```
#!/bin/bash


demoFun(){
    echo "这是我的第一个 shell 函数!"
}
echo "-----函数开始执行-----"
demoFun
echo "-----函数执行完毕-----"``

```

#Shell 文件包含

. filename   # 注意点号(.)和文件名中间有一空格

或

source filename

## 实例

创建两个 shell 脚本文件。

test1.sh 代码如下：



```
#!/bin/bash

url="http://www.runoob.com"

test2.sh 代码如下：

#!/bin/bash


#使用 . 号来引用test1.sh 文件
. ./test1.sh

# 或者使用以下包含文件代码
# source ./test1.sh

echo "菜鸟教程官网地址：$url"
```

