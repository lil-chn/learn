git config --global user.name "lil"
git config --global user.email "lil_chn@hotmail.com"

mkdir learngit
cd learngit
pwd

# 创建版本库
$ git init # 通过git init命令把这个目录变成Git可以管理的仓库
Initialized empty Git repository in /Users/michael/learngit/.git/

# 添加文件到Git
$ git add file1.txt 
# commit可以一次提交很多文件，所以你可以多次add不同的文件
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."


# 查看修改
$ git status # 要随时掌握工作区的状态，使用git status命令
$ git diff readme.txt # git diff可以查看修改内容


# 版本回退
git log # 查看版本
$ git reset --hard HEAD^ # 上几个的版本：HEAD~100
$ git reset --hard 1094a # 指定版本号
$ git reflog # git reflog用来记录你的每一次命令


# 管理修改
git diff HEAD -- readme.txt # 查看工作区和版本库里面最新版本的区别


# 撤销修改
git checkout -- readme.txt # 丢弃工作区的修改
git reset HEAD <file> # 回到最新版本


# 删除文件
rm test.txt
git status # git status命令会立刻告诉你哪些文件被删除
git rm test.txt # 确实删除
git commit -m "remove test.txt" # 还原


# 添加远程库
ssh-keygen -t rsa -b 2048 -C "lil-chn@hotmail.com" # 生成密钥
git remote add origin git@github.com:lil-chn/learngit.git
git push -u origin master
# -u会把本地的master分支和远程的master分支关联起来
git push -u origin master # 以后本地提交后就可以同步