1.��װgit
2.����ȫ���û���email
	--git config --global user.name "wuhuamian"
	--git config --global user.email "1746699469@qq.com"
3.�����汾��
	--cd D:->mkdir gitme->cd gitme->mkdir testgit->cd testgit->pwd(�鿴Ŀ¼)
	--git init
4.����ļ����ݴ����������
	--git add readme.txt(�����ļ�)
5.�ύ�ļ����ֿ�
	--git commit -m 'readme.txt pushed'(�ύ��ע)
6.�鿴�ύ״̬���Ƿ���δ�ύ
	--git status
7.�鿴�������ʲô����
	git diff readme.txt������֮��Ҫͨ��q�����˳���h������ʾ�������
8.ÿ���޸��궼����ִ��
	��==��git add readme.txt �� git commit -m "�ύ��ע����ѡ"
	��==��git commit -am "�ύ��ע"
	��==��git commit -a -m
ͨ�������ύgit��ʱ���ǣ�
	git add .(.�������У�Ҳ����ָ������ĳ���ļ�)
	git commit -m "�ύ��ע"
	git push
ʵ��������ֻ��ִ���������ɣ��������µ��ļ�Ҫ����ӽ���
	git commit -am "�ύ��ע"
	git push
9.�鿴commit��ʷ
	git log
	git log --pretty=oneline(����ʾ)
10.�鿴ĳ���ļ����޸���ʷ
	git log -p <filename>
	git log -p -2(�鿴������εĸ��µ�����)
11.�鿴ĳ��commit���޸�����
	git show <commit-hash-id> 
12.�汾����
	git reset --hard HEAD^(�˻���һ���汾)
	git reset --hard HEAD^^���˻�����һ���汾�������Դ����ƣ�
	git reset --hard HEAD~100���˻ص�ǰһ�ٸ��汾��
13.�汾�ظ�
	git reflog(�鿴���а汾��)
	git reset --hard �汾��
14.�鿴�ļ��е�����
	cat readme.txt

�������Ͱ汾��
	�汾�⣺.gitĿ¼
	���������Ͱ汾��ͬ���������ļ����ļ���

15.δ�ύ֮ǰ�����г����޸�
	a.ɾ�����޸ĵ����ݣ�ִ��git add  ��  git commit -m
	b.�˻ذ汾
	c.git checkout -- readme.txt��--����ո�
16.ɾ���ļ�
	a.ֱ����Ŀ¼��ɾ��
	b.rm readme.txt
û��commit֮ǰ����ʹ�� git checkout --readme.txt �Ӱ汾���лָ�
commit�򳹵�ɾ��

����Git�ֿ��github�ֿ�֮��Ĵ�����ͨ��SSH���ܵ�
17.����SSH key����
	ssh-keygen -t rsa -C "email��ַ"
	
���һ��Զ�̿�--create  a new repo.
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
18.�ڱ��ص�testgit�ֿ�������
	git remote add origin https://github.com/wuhuamian/testgit.git
19.�ڱ��زֿ��֧master�������͵�Զ�ֿ̲�
	git push -u origin master������Զ�̿��ǿյģ����ǵ�һ������master��֧ʱ�������� �Cu������Git������ѱ��ص�				master��֧�������͵�Զ���µ�master��֧������ѱ��ص�master��֧��Զ�̵�master��֧����				���������Ժ�����ͻ�����ȡʱ�Ϳ��Լ������
20.�����ύ
	git push origin master
===============================================================================
=========���������˽������б��ؿ⣬����Զ�̿��ʱ����ι���Զ�̿�============
===============================================================================
==================����������Զ�̿⣬Ȼ���¡��������===========================
21.��¡������
	git clone https://github.com/wuhuamian/whmrep.git(Զ�̿��ַ)

������ϲ���֧����ֹ��Ŀǰ��ֻ��һ��ʱ���ߣ���Git������֧������֧����master��֧��HEAD�ϸ���˵����ָ���ύ������ָ��master��master����ָ���ύ�ģ����ԣ�HEADָ��ľ��ǵ�ǰ��֧��

22.����dev��֧��Ȼ���л���dev��֧��
	git checkout -b dev
	��==��git branch dev�������� �� git checkout dev���л���
23.�鿴���з�֧	
	git branch
24.�л�����֧
	git checkout name
25.�ϲ�ĳ��֧����ǰ��֧
	git merge name
26.ɾ����֧
	git branch -d name

�����ͻ����
	1.git checkout -b fenzhi1
	2.�������
	3.�л���֧��master��
	4.���������
	5.master��֧�Ϻϲ�fenzhi1
���У�<<<<HEAD��ָ����֧�޸ĵ����ݣ�>>>>>>fenzhi1��ָfenzhi1���޸ĵ����ݡ�����
�鿴���ݣ��޸ĳɺ������ϵĴ���һ�����ɡ�

��֧�������
	ͨ���ϲ���֧ʱ��gitһ��ʹ��fast forward  ģʽ��������ģʽ�£�ɾ����֧�󣬻ᶪ����֧��Ϣ������ͨ��--no-ff���� fast forwardģʽ��
	1.����һ��dev��֧
	2.�޸�readme.txt����
	3.��ӵ��ݴ���
	4.�л�������֧��master��
	5.�ϲ�dev��֧��ʹ������git merge -no-ff -m "ע��" dev
	6.�鿴��ʷ��¼
��֧���ԣ�����master����֧Ӧ���Ƿǳ��ȶ��ģ�Ҳ�������������°汾��һ������²�����������ɻ�ɻ�һ����������½���dev��֧�ϸɻ����󣬱�����Ҫ����������˵dev��֧�����ȶ�����Ժϲ�������֧master������

bug��֧��
	�ڿ����У��ᾭ������bug���⣬��ô����bug����Ҫ�޸�����git�У���֧ʱ��ǿ��ģ�ÿ��bug������ͨ��һ����ʱ��֧���޸����޸���ɺ󣬺ϲ���֧��Ȼ����ʱ�ķ�֧ɾ������

27.git stash (����ǰ�Ĺ����ֳ���������)
28.git stash list (�鿴�����ֳ�)
29.git stash apply���ָ��ֳ���
30.git stash drop (ɾ���ֳ�)
31.git stash pop ���ָ���ͬʱɾ��stash���ݣ�

���˺�����
32.git remote ���鿴Զ�̿����Ϣ��
33.git remote -v ����ϸ��Ϣ��


���ͷ�֧��push �����ͣ� 
34.git push origin master
	fetch��ץȡ��



	

