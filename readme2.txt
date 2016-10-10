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
13.版本回复
	git reflog(查看所有版本号)
	git reset --hard 版本号
111111111111111
