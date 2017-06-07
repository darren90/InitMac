# InitMac
Mac Development environment init 


It is used for managing the snippets in xcode.

The default snippets are stored in the 

`~/Library/Developer/Xcode/UserData/CodeSnippets/`

# Git常用指令


## 1 : 配置

    # 显示当前的Git配置
    $ git config --list
    
## 2 ：代码提交  

    # 提交暂存区到仓库区
    $ git commit -m [message]



## 3 ：分支

    # 列出所有本地分支
    $ git branch
    
    # 列出所有远程分支
    $ git branch -r
    
    # 列出所有本地分支和远程分支
    $ git branch -a
    
    # 新建一个分支，但依然停留在当前分支
    $ git branch [branch-name]
    
    # 新建一个分支，并切换到该分支
    $ git checkout -b [branch]
    
    # 删除[branch]分支
    $ git branch -D [branch] 

## 4 ： 标签

    # 列出所有tag
    $ git tag
    
    # 新建一个tag在当前commit
    $ git tag [tag]
    
    # 新建一个tag在指定commit
    $ git tag [tag] [commit]
    
    # 删除本地tag
    $ git tag -d [tag]
    
    # 删除远程tag
    $ git push origin :refs/tags/[tagName]
    
    # 查看tag信息
    $ git show [tag]
    
    # 提交指定tag
    $ git push [remote] [tag]
    
    # 新建一个分支，指向某个tag
    $ git checkout -b [branch] [tag]

## 5 : 查看信息

    # 显示commit历史，以及每次commit发生变更的文件
    $ git log --stat
    
    # 搜索提交历史，根据关键词
    $ git log -S [keyword]
    
    # 显示所有提交过的用户，按提交次数排序
    $ git shortlog -sn

## 6 ： 远程仓库

    # 下载远程仓库的所有变动
    $ git fetch [remote]
    
    # 显示所有远程仓库
    $ git remote -v
    
    # 显示某个远程仓库的信息
    $ git remote show [remote]
    
    # 增加一个新的远程仓库，并命名
    $ git remote add [shortname] [url]
    
    # 取回远程仓库的变化，并与本地分支合并
    $ git pull [remote] [branch]
    
    # 上传本地指定分支到远程仓库
    $ git push [remote] [branch]
    
    # 强行推送当前分支到远程仓库，即使有冲突
    $ git push [remote] --force
    
    # 推送所有分支到远程仓库
    $ git push [remote] --all

## 7 ： 撤销
    
    # 恢复暂存区的指定文件到工作区
    $ git checkout [file]
    
    # 恢复某个commit的指定文件到暂存区和工作区
    $ git checkout [commit] [file]
    
    # 恢复暂存区的所有文件到工作区
    $ git checkout .
    
    # 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
    $ git reset [file]
    
    # 重置暂存区与工作区，与上一次commit保持一致
    $ git reset --hard
    
    # 重置当前分支的指针为指定commit，同时重置暂存区，但工作区不变
    $ git reset [commit]
    
    # 重置当前分支的HEAD为指定commit，同时重置暂存区和工作区，与指定commit一致
    $ git reset --hard [commit]
    
    # 重置当前HEAD为指定commit，但保持暂存区和工作区不变
    $ git reset --keep [commit]
    
    # 新建一个commit，用来撤销指定commit
    # 后者的所有变化都将被前者抵消，并且应用到当前分支
    $ git revert [commit]
    
    # 暂时将未提交的变化移除，稍后再移入
    $ git stash
    $ git stash pop

## 暂存

	#保存当前的工作进度。会分别对暂存区和工作区的状态进行保存
	git stash
	
	#显示进度列表。此命令显然暗示了git stash 可以多次保存工作进度，并用在恢复时候进行选择
	git stash list
	
	#恢复最新保存的工作进
	git stash pop [--index] [<stash>]

 	 # 删除所有存储的进度
	 git stash clear
	
	
## Git其他非常用，但需了解的操作

    # 取别的分支的某一次的提交
    git cherry-pick <commit id>

    # Git 把代码置到某一次的提交
     git checkout [<commit>]

	 恢复文件，取消对文件的修改
	 git checkout -- XXXX.m
	 git checkout -- <file>..." to discard changes in working directory
	
	//从暂存区删除,取消文件暂存，文件回到工作区
	use "git reset HEAD <file>..." to unstage
	git reset HEAD <file>
	
	  修改最后一次提交
	 git commit --amend



