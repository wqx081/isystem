### 在以普通用户打开的VIM当中保存一个ROOT用户文件

    :w !sudo tee %

命令:w!{cmd}，让vim执行一个外部命令{cmd}，然后把当前缓冲区的内容从stdin传入。

tee是一个把stdin保存到文件的小工具。

而%，是vim当中一个只读寄存器的名字，总保存着当前编辑文件的文件路径。

所以执行这个命令，就相当于从vim外部修改了当前编辑的文件，好完工。

***


### Pipe stderr

    spark-submit spark_sum_list.py 2>&1 | grep 24

***
