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
	git push -u origin master
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
111111111111111
