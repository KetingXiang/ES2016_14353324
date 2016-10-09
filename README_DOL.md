#DOL开发环境配置
##Description
The distributed operation layer(DOL) is a software development framework to program parallel  applications. The DOL allows to specify applications based on the Kahn process network model of computation and features a simulation engine based on SystemC. Moreover, the DOL provides an XML-based specification format to describe the implementation of a parallel application on a multi-processor systems, including binding and mapping.
##How to install
###安装必要的环境
	sudo apt-get update
	sudo apt-get install ant
	sudo apt-get install openjdk-7-jdk
	sudo apt-get install unzip
###解压文件
新建dol文件夹<br/>
	mkdir dol <br/>
将dolethz.zip解压到dol文件夹中<br/>
	unzip dol_ethz.zip -d dol <br/>
解压systemc<br/>
	tar -zxvf systemc-2.3-1.tgz <br/>
###编译systemc
解压后进入systemc-2.3.1的目录下<br/>
	cd systemc-2.3.1<br/>
新建一个临时文件夹objdir<br/>
	mkdir objdir<br/>
进入该文件夹<br/>
	cd objdir<br/>
运行configure<br/>
	../configure CXX=g++ --disable-async -updates<br/>
运行结果<br/>
![1](http://i1.piimg.com/567571/d105f8df41f9246d.png)
编译<br/>
	sudo make install<br/>
文件目录为:<br/>
![2](http://i1.piimg.com/567571/70e5cb7f759ea566.png)<br/>
记录当前的工作路径<br/>
![3](http://i1.piimg.com/567571/90bd424d3e17677a.png)<br/>
###编译DOL
	ant -f build_zip.xml all<br/>
![4](http://i1.piimg.com/567571/e5bd52021b905f7f.png)<br/>
###运行第一个例子
进入build/bin/mian路径下<br/>
	ant -f runexample.xml -Dnumber=1<br/>
![5](http://i1.piimg.com/567571/508b736cfd831004.png)<br/>

##Experimental experience
本次实验主要是需要耐心和足够的仔细，我一共配置了四遍才成功，总是在最后一步build不成功，从中犯过很多错误，包括拼写错误，已经Java环境变量的设置。最后也是实在不行重头来的一遍，删掉了所有东西才配置好的。

