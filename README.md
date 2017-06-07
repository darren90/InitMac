# InitMac
Mac Development environment init 


It is used for managing the snippets in xcode.

The default snippets are stored in the 

`~/Library/Developer/Xcode/UserData/CodeSnippets/`

## Git的[常用操作](https://github.com/darren90/InitMac/blob/master/Git%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4.md)

# Git提交操作
假如：项目名称XClient 项目主分支：master 当前自己的开发分支：ftf/dev
 
	 cd XClient
	 
	 git status
	 git add .
	 git commit -m "add new file"
	 # 这一步就要从远端拉取代码 ,先切到主分支
	 git checkout master
	 # 拉取代码
	 git pull 
	 # 切回自己的开发分支
	 git checkout ftf/dev
	 # 合并代码
	 git rebase ios
	 # 合并后提交刚才的提交
	 git push
	 ## 如果远端已经存在自己的ftf/dev，则强制提交
	 git push -f

### 本地切个分支 ，并提交
    git ch -b release-3.5.8
    git push
    
# zshrc配置 
	plugins=(git mvn brew osx python git-flow npm history)
    

//项目工程排序
perl PUClient/script/sort-Xcode-project-file PUClient/PUClient.xcodeproj/project.pbxproj



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






















