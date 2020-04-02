获取权限: sudo -i
修改密码: passwd
查看安全配置: nano /etc/ssh/sshd_config
修改配置: 
PasswordAuthentication yes
PermitRootLogin yes
重启配置: service ssh restart
更新命令工具: apt upgrade && apt update 
安装Ubuntu桌面: apt install ubuntu-desktop -y
安装虚拟视频驱动: apt install xserver-xorg-video-dummy -y
查看驱动配置: nano /etc/X11/xorg.conf
添加配置脚本:
Section "Device"
    Identifier  "Configured Video Device"
    Driver      "dummy"
EndSection
Section "Monitor"
    Identifier  "Configured Monitor"
    HorizSync 31.5-48.5
    VertRefresh 50-70
EndSection
Section "Screen"
    Identifier  "Default Screen"
    Monitor     "Configured Monitor"
    Device      "Configured Video Device"
    DefaultDepth 24
    SubSection "Display"
    Depth 24
    Modes "1600x900"
    EndSubSection
EndSection


Section "Monitor"
  Identifier "Monitor0"
  HorizSync 28.0-80.0
  VertRefresh 48.0-75.0
  # https://arachnoid.com/modelines/
  # 1920x1080 @ 60.00 Hz (GTF) hsync: 67.08 kHz; pclk: 172.80 MHz
  Modeline "1920x1080_60.00" 172.80 1920 2040 2248 2576 1080 1081 1084 1118 -HSync +Vsync
EndSection
Section "Device"
  Identifier "Card0"
  Driver "dummy"
  VideoRam 256000
EndSection
Section "Screen"
  DefaultDepth 24
  Identifier "Screen0"
  Device "Card0"
  Monitor "Monitor0"
  SubSection "Display"
    Depth 24
    Modes "1920x1080_60.00"
  EndSubSection






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

🎉 好了！可以远程连接了 😎



● 查看所有文件列表 
  ls -a -lh
  la -lh
  l -a -lh
  l

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

● 查看公网IP
curl ipinfo.io

● 强制重启  
sudo -i
reboot -p  立即关机重启
reboot -f  立即切断电源并重启

● 更新系统
sudo -i
apt dist-upgrade

● 查找占用指定端口号的进程编号 
sudo -i
lsof -i:8080
kill <pid>

● 

● 