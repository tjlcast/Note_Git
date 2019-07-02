git_command.md

#### key words
work_space	--add-->	|    stage  --commit--> master 	|
						|			repository 			|

#### create version repository
+ git init
+ git status
+ git add <...>
+ git commit <...>
+ git diff <...>
	+ 不加参数即默认比较工作区与暂存区
	+ --cached  [<path>...] 比较暂存区与最新本地版本库（本地库中最近一次commit的内容）
	+ HEAD [<path>...]  比较工作区与最新本地版本库

#### git history
+ git log
	+ --pretty=oneline
+ git reflog

#### revert change
+ git reset --hard HEAD^ 
	+ 切换HEAD指针{主要用于丢弃stage的change}
+ git checkout -- filename.txt
	+ 切换到最近一次add或commit{主要用于丢弃工作区的修改}

#### remote repository
- generate isa_pub and send it to github. 

+ git remote add origin git@github.com:michaelliao/learngit.git
	+ 关联到远端repo.

+  git branch --set-upstream-to=origin/master feature-A
	+ 把本地feature-A关联到origin/master.

+ git push -u origin feature
	+ 参数u，把本地的master分支和远程的master分支关联起来,然后push分支. 

+ git branch -r
	+ 远端库的分支

+ git push origin --delete Chapater6  
	+ 删除远端分支

+ git clone

#### branch manage and merge
+ git branch -a

+ git checkout -b dev
	+ 创建并切换分支
	+ git branch dev
	+ git checkout dev


