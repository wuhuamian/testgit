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
	git add readme.txt
	git commit -m "提交备注，可选"