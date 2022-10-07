git config --list
git config --list --show-origin
git help <verb>
git <verb> --help
man git-<verb>


git init


git add readme.txt

git commit -m "wrote a readme file"

git status

git diff readme.txt

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