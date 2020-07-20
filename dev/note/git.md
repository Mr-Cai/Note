● Git push 卡住  
全局  
> git config –global sendpack.sideband false  

仓库  
> git config –local sendpack.sideband false

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