● 修改jks密码
keytool -storepasswd -keystore xx.jks

● 打印jks信息
keytool -list -v -keystore xx.jks    

● 打印 RSA
keytool -printcert -file META-INF/CERT.RSA 

● ERROR 3680 (HY000): Failed to create schema directory 'hive' (errno: 13 - Permission denied)
chown -R mysql:mysql /usr/local/mysql/data

●  Warning:"config" scripts ...
sudo rm -rf /Library/Frameworks/Python.framework

● building Homebrew formulae, and may need to be deleted.

● Permission denied @ apply2files
sudo chown -R $(whoami):admin /usr/local/* \
&& sudo chmod -R g+rwx /usr/local/*

● Updating Homebrew... 很慢
Ctrl+C

● [oh-my-zsh] Insecure completion-dependent directories detected:
chmod 755 /usr/local/share/zsh
chmod 755 /usr/local/share/zsh/site-functions

● mysql 远程登录
mysql -uroot -h106.53.106.142 -p


● SQL生成MD5随机串
SELECT
substring(
  MD5(RAND()),1,16 
)

● Windows 环境变量
set NAME=<PATH>|<URL>
eg: set ADB=C:\Users\M\Documents\adb\
set CON=https://example.com.cn

● Windows 打印程序路径
 (Get-Command xx.exe).Path
 
● 