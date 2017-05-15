# InitMac
Mac Development environment init 


It is used for managing the snippets in xcode.

The default snippets are stored in the 

`~/Library/Developer/Xcode/UserData/CodeSnippets/`

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


























