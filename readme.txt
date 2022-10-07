git config --list
git config --list --show-origin
git help <verb>
git <verb> --help
man git-<verb>


git init


git add readme.txt

git commit -m "wrote a readme file"

#跳过暂存区直接提交
git commit -a 

git status

当前文件和暂存区域快照之间的差异， 也就是修改之后还没有暂存起来的变化内容
git diff readme.txt

已暂存的将要添加到下次提交里的内容
git diff --staged

查看工作区和版本库里面最新版本的区别，比对已暂存文件与最后一次提交的文件差异
git diff HEAD -- readme.txt

命令显示从最近到最远的提交日志
git log 
简化日志（包括commit id 版本号和 commit 以及head 指向的版本）
git log --pretty=oneline

HEAD表示当前版本，上一个版本就是HEAD^，上上一个版本就是HEAD^^，上100个版本 HEAD~100
回退至上一个版本
git reset --hard HEAD^
回退至某个版本，指定commit id 前几位
git reset --hard 1094a

查看命令历史
git reflog

丢弃工作区的修改(回到与版本库或者暂存区一致的版本)  注意是两个-
git checkout -- readme.txt
git restore readme.txt

只能做到在工作区删除
rm temp.md

工作区和仓库同时删除，但需要commit进行提交
git rm temp.md

把文件从 Git 仓库中删除（亦即从暂存区域移除），但仍然希望保留在当前工作目录中
这些文件可忽略，或者是存在于.gitignore中
git rm --cached README

移动文件
git mv LICENSE LICENSE.txt
等价于下面三条命令
mv LICENSE LICENSE.txt
git rm LICENSE
git add LICENSE.txt

暂存区的修改撤销掉（unstage），重新放回工作区 即从已暂存返回已修改状态
git restore --staged  LICENSE
会发现LICENSE被删除，有个新文件LICENSE.txt
git restore LICENSE           丢弃工作区的修改
会发现LICENSE已经还原，此时也有个新文件LICENSE.txt

