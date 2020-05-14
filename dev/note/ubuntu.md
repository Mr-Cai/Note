获取权限: sudo -i

修改密码: passwd

查看安全配置: nano /etc/ssh/sshd_config

● 修改登录配置: 
PasswordAuthentication yes
PermitRootLogin yes
PubkeyAuthentication yes

重启配置: service ssh restart

更新命令工具: apt upgrade && apt update 

● 安装Ubuntu桌面:
安装Ubuntu桌面: apt install ubuntu-desktop -y
安装虚拟视频驱动: apt install xserver-xorg-video-dummy -y
查看驱动配置: nano /etc/X11/xorg.conf
添加配置脚本:

Section "Device"
        Identifier "Configured Video Device"
EndSection

Section "Monitor"
        Identifier "Configured Monitor"
EndSection

Section "Screen"
        Identifier "Default Screen"
        Monitor "Configured Monitor"
        Device "Configured Video Device"
        SubSection "Display"
                   Depth 24
                   Virtual 1920 1080
        EndSubSection
EndSection


重启服务器: reboot
获取权限: sudo -i 
安装Gdebi包管理器: apt install gdebi -y
切换目录: cd /tmp
从网站下载包: wget https://download.teamviewer.com/download/linux/teamviewer_amd64.deb
安装TeamViewer: gdebi teamviewer_amd64.deb
teamviewer license accept 授权
teamviewer daemon enable 激活自启动
teamviewer daemon start 开启服务
teamviewer passwd xxxx 设置访问密码
teamviewer info 查看连接信息

● 查看所有文件列表 
  ls -a -lh
  la -lh
  l -a -lh
  l
  ll
  ll -h
  ls

● 获取管理员权限 sudo -i 

● 删除不常用软件
sudo -i
rm -rf /usr/share/applications/com.canonical.launcher.amazon.desktop /usr/share/applications/ubuntu-amazon-default.desktop
apt purge -y libreoffice-common thunderbird* firefox deja-dup simple-scan hplip* 
apt purge -y printer-driver* rhythmbox* gedit* libreoffice* onboard mahjongg aisleriot gnomine wodim 
apt purge -y gnome-orca gnome-sudoku gnome-startup-applications gnome-todo remmina*
apt purge -y cheese gnome-power-manager gnome-mahjongg gnome-calendar gnome-video-effects 
apt purge -y shotwell transmission* ubuntu-software* ubuntu-sounds* htop gnome-screenshot
apt purge -y gnome-terminal* xterm* gnome-software*

● 安装中文简体
sudo -i
系统语言汉化包 apt install language-pack-zh-hans language-pack-zh-hans-base language-pack-gnome-zh-hans language-pack-gnome-zh-hans-base
软件语言中文包 apt install `check-language-support -l zh` -y
设置默认为中文 localectl set-locale LANG=zh_CN.UTF-8
重启 reboot

● 清理老旧垃圾
apt autoremove

● ssh上传、下载文件
上传:  scp path/file.xx root@106.53.106.142:/user/path
下载:  scp root@106.53.106.142:/user/path/file.xx path/
文件夹: scp -r 

● 后台运行Jar
nohub java -jar xx.jar &  # 简易
nohup java -jar /user/path/xx.jar >/user/path/xx.log 2>&1 & # 完整

● 关闭后台运行Jar
jobs # 查看后台任务编号
fg 0 # 切换指定编号到前台
ctrl + c

● 关闭shell脚本中的jar进程
● ps -ef | grep java
● kill 编号

● 开机自启动脚本

● 升级系统
apt upgrade && apt update -y
do-release-upgrade
