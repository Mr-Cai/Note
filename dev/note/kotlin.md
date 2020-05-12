🦠 ktor项目打不开
> 检查SDK路径是否未定义，有时会自动清空
> 清理 .idea 或清理 *.ipr
> 修改 gradle版本为本地的版本
> ./gradlew run

🦠 ktor下载依赖库失败
> 例: Could not resolve io.ktor:ktor-client-http-timeout:1.3.2
> 检查失败下载对应的包名，是否引用了ktor_version
> 搜索失败下载的仓库源地址，替换现存版本尝试
> 搜索不到就注释掉

🦠 地址已经被使用
> Exception in thread "main" java.net.BindException: Address already in use
> 检查是否有另一个gradle 进程在使用，并关闭
> ./gradlew --stop
> ./gradlew clean
> 关闭翻墙软件

🦠 0.0.0.0 无响应
> 检查端口号是否被占用
> 查找占用端口 lsof -i:80
> 关闭占用端口 kill 2514
> 清除浏览器缓存，强制http，检查浏览器开头是否重定向为https
> 代码中检查是否有重定向为https的配置
> 实在不行换一个端口号


🦠 
🦠 
🦠 
🦠 
🦠 
🦠 