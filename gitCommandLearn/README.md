[TOC]

# 学习git操作
## git 工具安装
> Linux： sudo apt-get install git  
Window:到Git官网下载安装：[链接](https://git-scm.com/downloads)
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
git commit -am 'desc' -a all所有
  #### commit的反操作 $git reset
> 撤销提交comnmit
$git reset --hard HEAD^回退到上个版本  
$git reset --hard HEAD~ 3回退到前3次提交之前，以此类推，回退到n次提交之前  
$git reset --hard commit_id 退到/进到 指定commit的sha码  
如果没有别的操作，直接回到上一次提交就可以了，在a分支执行  
git reset --hard HEAD~ 会回到未merge前的状态，清空暂存区，销毁数据，如果没有推送到远程，  
数据就会被覆盖无法恢复，如果已推送远程，可以通过 reflog 找回。  
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
### $ git checkout -b newBranch
> 创建并切换到newBranch分支
### 添加ignore文件管理
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
### $git reflog
> 查看更新的版本日志
### git log 
> 查看历史提交记录
