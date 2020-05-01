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