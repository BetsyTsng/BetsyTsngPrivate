# Debian11+Gnome系统安装后配置

1.设置“终端”的快捷键：设置->键盘快捷键->自定义快捷键->点击加号->[名称：终端; 命令：gnome-terminal; 快捷键：Ctrl+Alt+T]

2.安装KeePassXC->自带的软件商店便有

3.安装GCC(VMware所需要的依赖)

```
sudo apt update
sudo apt install build-essential
sudo apt-get install manpages-dev
gcc --version
```

4.安装Linux Kernel headers(VMware所需要的依赖)

```
sudo apt-get install linux-headers-$(uname -r)
```

5.配置OpenVPN

```
apt-get install openvpn
apt-get install network-manager-openvpn-gnome
```

6.安装nvidia官方驱动 

https://wiki.debian.org/NvidiaGraphicsDrivers#Debian_11_.22Bullseye.22wiki.debian.org/NvidiaGraphicsDrivers#Debian_11_.22Bullseye.22

7.安装Python

https://www.python.org/downloads/source/

a.安装

```
   sudo apt-get install openssl
    sudo apt-get install libssl-dev #解决：python ImportError: No module named _ssl
   ./configure --enable-optimizations
    make
    make test
    sudo make install
```

b.测试

```
python3 --version
idle3
```

如果出现tkinter # If this fails your Python may not be configured for Tk

则

```
sudo apt install python3-tk
sudo apt install tk-dev
```

出现 

Could not fetch URL https://pypi.org/simple/you-get/: There was a problem confirming the ssl certificate: HTTPSConnectionPool(host='[pypi.org](http://pypi.org/)', port=443): Max retries exceeded with url: /simple/you-get/ (Caused by SSLError("Can't connect to HTTPS URL because the SSL module is not available.")) - skipping

换源

https://www.ucloud.cn/yun/43372.html