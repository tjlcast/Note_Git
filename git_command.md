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

#### remote repo

