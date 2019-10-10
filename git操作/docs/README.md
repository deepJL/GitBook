# git

## 版本回退

基于索引值前进后退

```
----可往前可往后-------
git reflog

git reset --hard 9a9ebe0 

-----可后退不能往前--------
git reset --hard HEAD^^^  等同于 git reset --hard HEAD~3

注：总的来说还是第一种方法好


```

练习：

- git reflog
- git reset --hard ……

-----

> git add 文件名后 但还没有commit 如何回退
>
> git reset hard HEAD 

> 比较文件差异
>
> git diff apple.txt（和暂存区比较） 如果git add 后用这个命令不显示啥

> git diff apple.txt HEAD apple.txt（和本地版本库作比较）
>
> 也就是git add 后还用该命令还是能够显示出不同

> git diff HEAD^ （和版本库中上一个版本比较）

> git diff HEAD (和多个版本比对)

 

修复主分支上面的bug  ,一般建一个hot_fix



## 分支操作

>  git branh -v（分支信息）

> git branch hot_fix

> git checkout hot_fix （切换分支）

> （分支合并到master 上面）
>
> 先切换到master 上面
>
> git checkout master
>
> 然后 
>
> git merge hot_fix  (这样就合并到master 上面了)

> git merge 出现冲突
>
> 删掉冲突后
>
> git add 文件名
>
> 然后用
>
> git commit -m ' '(不要带文件名)

## 上传远程仓库

先创建远程仓库  复制htts 的连接git 的连接不管用
在要上传的文件夹下 
git init
将文件复制过来
git add 
git commit -m ''    先传到版本库中再将
git remote add origin https://gitlab.golaxy.cn/wangxiaowen/wxw_test.git

（删除 git remote remove origin）

再用git push origin master 就行了

## 克隆

git clone ……



## 团队操作

先得加入团队

在项目的setting 中点击合作者 ，输入合作者的名字，然后复制分享链接，合作者打开连接就行了。这样就有写的权限了。



注： push 的时候第一次要输入用户名密码第二次不用输入 这是因为

winows 自带的凭据管理的的作用。 删除账号直接凭据管理器中删除。



## 远程库的修改的拉取

pull 相当与fetch 和  merge 的合并操作

git fetch origin master 先拉取下来但是不和并现在文件还是原来的

要查看拉取先来的还可以使用 git checkout origin master

切换回来 git checkout master

我习惯直接用pull 拉取 注意commit 的时候不带文件名

注： origin 是远程库地址别名 master 是远程分支名



## 跨团队协作

顾名思义就是跨团队操作

外部人员fork 项目：

外部人员获取到 

修改再push 到外部人员的fork 的库中

然后点击pull request 然后点击new pull request 

点击create pull request

然后小栏中写标贴 大的文本栏中写详细

这样提交完后

内部人员的项目pull request 那就有1的显示

点进来可以留言，点到commits 可以看具体的提交

在对话那有个merge pull request

之后在小栏中填写commit 的信息提交就行



## 如果想变提交路径 

修改 remote 的地址

git remote remove origin （可以用git remote  -v 去查看）

然后git remote add origin 连接 去添加 （当然不去除origin 另起一个也行）

push 就行

## eclipse 初始化本地库

### 工程初始化为本地库

项目右键 term -> share project -->先点击Use or create repository

![1570621015401](.\img\1570621015401.png)

![1570621125371](.\img\1570621125371.png)





eclipse 特定文件

一般要忽略特定的文件

如：   .classpath 文件

.project 文件

.setting 目录下的所有文件

target 文件

我写的文件在 C:\Users\14148\Java.gitignore

----

将目录文件提交到本地版本库

右键term -> add to Index

目录上面显示* 表示暂存 文件显示+ 表示文件暂存

然后 commit …… 写commit信息就提交了

之后提交直接按快捷键ctrl +# 



## elcipse 提交到远程库

term - > remote->push  填写信息 提交就行



## elcipse 克隆到本地

项目栏 空白处右键 选择import >import…… > Git> Projects from Git >

然后看着操作 > 填写上工作去的目录> 下一步后就下载下来了> 之后会问你

如何导入选择第三个（Import as general project）> ……

之后会导入进来但是目录结构不对不能直接用所有要转关成项目的目录结构

右键选择Configure 》 Convert to maven Preoject 

![1570635205392](.\img\1570635205392.png)



## 在eclipse 中解决冲突

 右键team 》拉取pull 拉下来显示冲突

可以点击右键 team > merge Tool 

显示自己的内容（左边）和远程库的内容（右边）

然后用快捷键 ctrl +# 就行 拖下来提交就行



## git 工作流

- 集中式（用的少）

![1570638188605](.\img\1570638188605.png)

- GitFlow 

  ![1570673892191](.\img\1570673892191.png)

![1570673978093](.\img\1570673978093.png)





## elcipse 分支

新建一个分支

 ![1570675391894](.\img\1570675391894.png)



![1570675414985](.\img\1570675414985.png)



切换分支审查代码：

 ![1570675435841](.\img\1570675435841.png)



![1570675809088](.\img\1570675809088.png)

![1570675820946](.\img\1570675820946.png)

检出远程新分支

![1570675839833](.\img\1570675839833.png)	

## 和并分支

- 合并分支切换为master 

  ![1570676065447](.\img\1570676065447.png)

- 合并分支

先切换为master 

![1570676346990](.\img\1570676346990.png)

合并分支

 ![1570676098488](.\img\1570676098488.png)

之后可选从本地的分支合并还是远程的分支合并

之后如果有冲突看前面的处理

之后提交完事

END









 