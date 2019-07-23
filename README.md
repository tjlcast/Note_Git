hello world. 
this is a begining. 
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

+ git log --graph

+ git merge dev
	+ dev分支的工作成果合并到当前分支

#### save the work space
+ git stash 
	- save the work space
+ git stash list 
	- list the items have been saved
+ git stash pop
	- remove and apply the item to current space
+ git stash apply
	- apply the item to current space
	
#### work space
+ git clean -n
	- remind you of the files will deleted
+ git clean -f 
	- forece to delete the files **(untracked files)**
	
#### example

##### work on dev
+ pre: you work is finished on your branch(jialtang_paging_local)
+ git branch -vv	// for example you on branch:jialtang_paging_local
+ git checkout -b jialtang_paging_pr origin/develop	// the branch:origin/develop is you base.
	- in other word `checkout -b [b1] [b2]` means the new branch b2 is based on b1.
+ git pull
+ git branch -vv					// 显示当前分支与远端分支的关系
+ git merge jialtang_paging_local --no-commit --no-ff	// merge but not commit so you can see stash and work space diff
+ git reset						// means you can see what haven you done on jialtang_paging_pr branch 
+ now you can see want you have done by "git status"
+ git reset *.config 					// 把本地环境的依赖删除
+ git commit -m "The function of paging locations table"// 只把暂存取的内容提交
+ Now clean current branch via `git checkout -- .`/`git reset`/`git clean`
+ git push origin jialtang_paging_pr			// push your code
