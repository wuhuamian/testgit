1.安装git
2.设置全局用户和email
	--git config --global user.name "wuhuamian"
	--git config --global user.email "1746699469@qq.com"
3.创建版本库
	--cd D:->mkdir gitme->cd gitme->mkdir testgit->cd testgit->pwd(查看目录)
	--git init
4.添加文件到暂存区（哪里？）
	--git add readme.txt(具体文件)
5.提交文件到仓库
	--git commit -m 'readme.txt pushed'(提交备注)
6.查看提交状态，是否还有未提交
	--git status
7.查看具体改了什么内容
	git diff readme.txt（命令之后，要通过q进行退出，h可以显示所有命令）
8.每次修改完都必须执行
	《==》git add readme.txt 和 git commit -m "提交备注，可选"
	《==》git commit -am "提交备注"
	《==》git commit -a -m
通常我们提交git的时候都是：
	git add .(.代表所有，也可以指定具体某个文件)
	git commit -m "提交备注"
	git push
实际上我们只有执行两条即可，除非有新的文件要被添加进来
	git commit -am "提交备注"
	git push
9.查看commit历史
	git log
	git log --pretty=oneline(简单显示)
10.查看某个文件的修改历史
	git log -p <filename>
	git log -p -2(查看最近两次的更新的内容)
11.查看某次commit的修改内容
	git show <commit-hash-id> 
12.版本回退
	git reset --hard HEAD^(退回上一个版本)
	git reset --hard HEAD^^（退回上上一个版本。。。以此类推）
	git reset --hard HEAD~100（退回到前一百个版本）
13.版本回复
	git reflog(查看所有版本号)
	git reset --hard 版本号
14.查看文件中的内容
	cat readme.txt

工作区和版本库
	版本库：.git目录
	工作区：和版本库同级的所有文件和文件夹

15.未提交之前，进行撤销修改
	a.删除掉修改的内容，执行git add  和  git commit -m
	b.退回版本
	c.git checkout -- readme.txt（--后面空格）
16.删除文件
	a.直接在目录下删除
	b.rm readme.txt
没有commit之前可以使用 git checkout --readme.txt 从版本库中恢复
commit则彻底删除

本地Git仓库和github仓库之间的传输是通过SSH加密的
17.创建SSH key命令
	ssh-keygen -t rsa -C "email地址"
	
添加一个远程库--create  a new repo.
--create a new repository on the command line
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin https://github.com/wuhuamian/testgit.git
	git push -u origin master

--push an existing repository from the command line
	git remote add origin https://github.com/wuhuamian/testgit.git
	git push -u origin master
--import code from another repository
18.在本地的testgit仓库下运行
	git remote add origin https://github.com/wuhuamian/testgit.git
19.在本地仓库分支master内容推送到远程仓库
	git push -u origin master（由于远程库是空的，我们第一次推送master分支时，加上了 –u参数，Git不但会把本地的				master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联				起来，在以后的推送或者拉取时就可以简化命令。）
20.本地提交
	git push origin master
===============================================================================
=========以上我们了解了先有本地库，后有远程库的时候，如何关联远程库============
===============================================================================
==================以下是先有远程库，然后克隆到本地中===========================
21.克隆到本地
	git clone https://github.com/wuhuamian/whmrep.git(远程库地址)

创建与合并分支：截止到目前，只有一条时间线，在Git里，这个分支叫主分支，即master分支。HEAD严格来说不是指向提交，而是指向master，master才是指向提交的，所以，HEAD指向的就是当前分支。

22.创建dev分支，然后切换到dev分支上
	git checkout -b dev
	《==》git branch dev（创建） 和 git checkout dev（切换）
23.查看所有分支	
	git branch
24.切换到分支
	git checkout name
25.合并某分支到当前分支
	git merge name
26.删除分支
	git branch -d name

解决冲突问题
	1.git checkout -b fenzhi1
	2.添加内容
	3.切换分支（master）
	4.在添加内容
	5.master分支上合并fenzhi1
其中，<<<<HEAD是指主分支修改的内容，>>>>>>fenzhi1是指fenzhi1上修改的内容。。。
查看内容，修改成和主干上的代码一样即可。

分支管理策略
	通常合并分支时，git一般使用fast forward  模式，在这种模式下，删除分支后，会丢到分支信息，可以通过--no-ff禁用 fast forward模式。
	1.创建一个dev分支
	2.修改readme.txt内容
	3.添加到暂存区
	4.切换回主分支（master）
	5.合并dev分支，使用命令git merge -no-ff -m "注释" dev
	6.查看历史记录
分支策略：首先master主分支应该是非常稳定的，也就是用来发布新版本，一般情况下不允许在上面干活，干活一般情况下在新建的dev分支上干活，干完后，比如上要发布，或者说dev分支代码稳定后可以合并到主分支master上来。

bug分支：
	在开发中，会经常碰到bug问题，那么有了bug就需要修复，在git中，分支时很强大的，每个bug都可以通过一个临时分支来修复，修复完成后，合并分支，然后将临时的分支删除掉。

27.git stash (将当前的工作现场隐藏起来)
28.git stash list (查看工作现场)
29.git stash apply（恢复现场）
30.git stash drop (删除现场)
31.git stash pop （恢复的同时删除stash内容）

多人合作：
32.git remote （查看远程库的信息）
33.git remote -v （详细信息）


推送分支：push （推送） 
34.git push origin master
	fetch（抓取）



	

