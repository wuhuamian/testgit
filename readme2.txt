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
	git push -u origin master
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
13.版本恢复
	git reflog(查看所有版本号)
	git reset --hard 版本号
14.git log --pretty=oneline(列出所有提交的备注)
15.cat filename (退回版本后进行查看详情。。。)
16.git reflog (查看每次提交的版本号)
17.git reset --hard 版本号（恢复某次回退的内容）
18.git checkout -- filename(丢弃工作区的修改)
19.rm  file  (彻底从版本库中删除掉文件，紧接着执行commit)
20.git push -u[第一次推送] origin master
截止到目前，只有一条时间线，在git里，这个分支叫主分支，即master分支。HEAD严格来说不是指向master，master才是指向提交的，所以，HEAD指向的就是当前分支。
21.git checkout -b dev （创建并切换分支）《==》
22.git branch dev  git checkout dev
23.git branch （查看分支）
111111111111111
222222222222222
333333333333333
444444444444444
555555555555555
