#DOL实例分析与编程
##关于路径
修改文件的路径在：dol/examples</br>
运行文件的路径在：dol/build/bin/main</br>
运行文件的指令为：ant -f runexample.xml -Dnumber=X，X表示第几个样例。
##修改example1
打开square.c文件，源文件中i * i表示二次方，改成i * i * i就是表示三次方了。
输出结果为：</br>
![1](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/51585901.jpg)
</br>
##修改example2
在xml文件中我们可以看到：</br>
![2](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/46218690.jpg)
</br>
在这里我们可以看到一个迭代，我们只需要修改迭代次数的值：
![3](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/64289017.jpg)
</br>
运行结果为：</br>
![4](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/25159551.jpg)
</br>
##解锁文件权限
在修改源文件之后，需要删除编译后的文件，但是文件被加锁了不能直接删除，需要进入该文件的目录下：</br>
![5](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/8374241.jpg)
</br>
##查看新生成的.dot图
首先需要安装xdot软件才能查看dot文件</br>
![6](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/42031638.jpg)
</br>
example1:</br>
![7](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/8597322.jpg)
</br>example2:</br>
![8](http://7xrn7f.com1.z0.glb.clouddn.com/16-11-2/87669097.jpg)
##实验感想
理解了生产者，消费者，处理模块等这些进程的功能定义与其之间的互相关系。知道了C语言代码的实现方式以及XML中的实现方式，学会了怎样查看.dot文件。

