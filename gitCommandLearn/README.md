# gitLearn
学习git操作
## 操作命令 
### $mkdir 
> 创建本地目录
### $git init 
> 初始化本地仓库
### $git status 
> 查看本地状态
### $git add file
>添加file到git 管理 
### $git commit file -m "desc" 
>提交修改内容
### $git fetch
>获取获取最新到本地但不merge 
### $git pull 
> 拉取代码并merge
### $git push
> 推送提交内容到远程仓库
### $git diff
> 比较修改内容
### $git branch
> 查看分支情况 并高亮当前的分支
### $git branch newBranch
> 创建新分支
### $git checkout newBranch
> 切换分支
## 添加ignore文件管理
> gitignore文件内容的规则
/表示目录,比如/A/*就表示忽略A目录下所有内容  
*表示匹配多个字符,上面忽略A目录下所有内容使用的就是*，忽略iml结尾的文件即使用*.iml  
    []表示匹配多个单个字符,[abc]就是代表a、b、c中任何一个字符即可  
    ! 表示跟踪某类文件 比如 /*，!*.c，表示忽略所有文件，但是跟踪.c结尾的文件，这样.c结尾的文件就不会被忽略了  
    在使用.gitignore文件后如何删除远程仓库中以前上传的此类文件而保留本地文件  
    比如我们在使用git和github的时候，之前没有写.gitignore文件，就上传了一些没有必要的文件,  
    在添加了.gitignore文件后，就想删除远程仓库中的文件却想保存本地的文件。  
    这时候不可以直接使用git rm directory，这样会删除本地仓库的文件。  
    可以使用git rm -r –cached directory来删除缓冲，然后进行commit和push，这样会发现远程仓库中的不必要文件就被删除了，  
    以后可以直接使用git add -A来添加修改的内容，上传的文件就会受到.gitignore文件的内容约束。
