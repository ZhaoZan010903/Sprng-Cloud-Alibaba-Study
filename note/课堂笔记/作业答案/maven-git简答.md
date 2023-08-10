# maven-git简答

答案

```txt
以下所有问题全部基于课程笔记,但是答案需要自己理解的叙述

不能粘贴笔记内容.

MAVEN

1.maven项目管理工具作用是什么?
管理开发项目的工具,让多人协作开发变得简单.因为他将项目的完整生命周期,包括多模块关系都实现了统一管理

2.maven多模块特性有哪些(课堂讲解内容)
依赖,继承,聚合

3.简单描述一下maven的依赖?
多模块管理依赖关系,意义在于可以实现代码复用.
依赖特点具备传递性,但是可以通过去除实现精简的依赖

4.简单描述一下maven的聚合?
聚合的意义在于统一多模块的命令执行,不需要一个一个执行
聚合的实现是通过聚合工程,将聚合子工程的pom通过module配置在一起.
聚合子工程不需要做配置已操作

5.简单描述一下maven的继承?
继承的意义在于统一项目中多模块的资源版本
实现是通过父工程指定打包类型,子工程指向父工程parent完成的

6.以下maven生命周期的命令都是什么作用

clean ,compile,test,package,install,deploy
clean清空编译输出文件target
compile编译项目代码输出class到target
test执行单元检测
package项目打包
install项目安装到本地库
deploy发布到私服

7.镜像和远程中央库是什么关系?
通过配置镜像,使maven项目的资源通过镜像获取,一般镜像需要代理中央库

8.为什么公司要自己搭建maven私服,不直接使用远程中央库的资源?
中央库保存的是开源资源
公司私服保存公司私有资源

9.现在有AB两个人,A开发的项目a.jar包,交给B开发的项目依赖使用,请问如何实现?简述一下基本流程
A项目打包,安装到本地库,发布到远程私服
B项目配置dependency指向A项目坐标,从私服下载到本地库使用

10. 在工作中,maven执行命令出现错误,如何定位错误?
maven命令 添加选项-X 查看具体错误提示信息从而定位.
GIT

1.git练习案例

请按照如下要求,完成git练习(该题目请提交命令执行history)

a. 创建多分支
git branch a
git branch b

b. 各分支提交不同文件版本
git checkou a
git add *
git commit -m 'a'
git checkout b
git add *
git commit -m 'b'

c. 有意产生分支冲突
git checkout a
添加编辑文件a.txt
git checkout b
添加编辑文件a.txt
保证文件有行冲突

d. 合并解决冲突
git merge a
解决冲突
git add *
git merge --continue

2. 解释下面git命令的作用

a. git branch
查看分支

b. git branch b
创建分支 b

c. git add ./demo.txt
将demo.txt添加到暂存区

d. git commit -m "commit"
提交版本 附带描述 commit

e. git checkout branch1
切换到分支branch1

f. git merge branch1
当前分支(不能是branch1)
合并目标分支branch1

g. git log
查看当前分支当前版本之前的所有提交信息

h. git reflog
查看当前分支所有版本操作的日志

i. git reset --soft a93nd73b
通过soft方式回滚到version为a93nd73b
会保留当前版本和目标版本的差别文件到暂存区
```

```txt


```

