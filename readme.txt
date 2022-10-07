git config --list
git config --list --show-origin
git help <verb>
git <verb> --help
man git-<verb>


git init


git add readme.txt

git commit -m "wrote a readme file"

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


11112