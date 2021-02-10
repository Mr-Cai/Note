● Git push 卡住  
全局  
> git config --global sendpack.sideband false

仓库  
> git config –-local sendpack.sideband false

● Git 删除远程分支无效  
> git fetch -p origin     
> git push --delete origin origin/branch-name

● Git 更新忽略规则
> git rm -rf --cached . 
> git commit -am msg
> git push

● Git 代理连接被拒
Failed to connect to 127.0.0.1 port xxx: Connection refused
> git config --global --unset http.proxy
> git config --global --unset https.proxy
> git push --set-upstream origin master

● Git 克隆过慢, 克隆超时
设置代理端口为翻墙软件端口
> git config --global http.https://github.com.proxy socks5://127.0.0.1:7890

● Git 拉取卡住
清除缓存垃圾
> git gc --prune=now.

● Git 无法访问Gist
fatal: unable to access 'https://gist.github.com/xx.git/': Failed to connect to gist.github.com port 443: Timed out
> 

● Git 下载指定文件/文件夹
> git init [folderName] && cd [folderName]
> git remote add -f origin [repositoryURL]
> git config core.sparseCheckout true
> git sparse-checkout set [folderName]
> git pull origin [branchName] 
