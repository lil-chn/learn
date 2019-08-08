git config --global user.name "lil"
git config --global user.email "lil_chn@hotmail.com"

mkdir learngit
cd learngit
pwd

# �����汾��
$ git init # ͨ��git init��������Ŀ¼���Git���Թ���Ĳֿ�
Initialized empty Git repository in /Users/michael/learngit/.git/

# ����ļ���Git
$ git add file1.txt 
# commit����һ���ύ�ܶ��ļ�����������Զ��add��ͬ���ļ�
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."


# �鿴�޸�
$ git status # Ҫ��ʱ���չ�������״̬��ʹ��git status����
$ git diff readme.txt # git diff���Բ鿴�޸�����


# �汾����
git log # �鿴�汾
$ git reset --hard HEAD^ # �ϼ����İ汾��HEAD~100
$ git reset --hard 1094a # ָ���汾��
$ git reflog # git reflog������¼���ÿһ������


# �����޸�
git diff HEAD -- readme.txt # �鿴�������Ͱ汾���������°汾������


# �����޸�
git checkout -- readme.txt # �������������޸�
git reset HEAD <file> # �ص����°汾


# ɾ���ļ�
rm test.txt
git status # git status��������̸�������Щ�ļ���ɾ��
git rm test.txt # ȷʵɾ��
git commit -m "remove test.txt" # ��ԭ


# ���Զ�̿�
ssh-keygen -t rsa -b 2048 -C "lil-chn@hotmail.com" # ������Կ
git remote add origin git@github.com:lil-chn/learngit.git
git push -u origin master
# -u��ѱ��ص�master��֧��Զ�̵�master��֧��������
git push -u origin master # �Ժ󱾵��ύ��Ϳ���ͬ��