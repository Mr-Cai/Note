预备
    sudo -i
    apt update && apt upgrade -y
    apt install wget -y

Shadowsocks
    wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh && chmod +x shadowsocks-all.sh
    ./shadowsocks-all.sh

v2ray    
    bash <(curl -L -s https://install.direct/go.sh)
    service v2ray start
    cat /etc/v2ray/config.json
    
BBR 加速
    wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
    wget https://raw.githubusercontent.com/flyzy2005/ss-fly/master/v2ray.sh && chmod +x v2ray.sh && ./v2ray.sh -bbr


