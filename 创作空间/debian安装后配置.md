[Fcitx5安装教程](https://link.zhihu.com/?target=https%3A//wiki.debian.org/zh_CN/I18n/Fcitx5) [VSCODE安装教程](https://link.zhihu.com/?target=https%3A//wiki.debian.org/VisualStudioCode) [NvidiaGraphicsDrivers](https://link.zhihu.com/?target=https%3A//wiki.debian.org/NvidiaGraphicsDrivers)

总脚本

```bash
su root
apt install --install-recommends apt-transport-https telegram-desktop fcitx5 fcitx5-chinese-addons curl keepassxc openvpn network-manager-openvpn wget nvidia-detect nvidia-driver 
apt-get update
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
install -o root -g root -m 644 microsoft.gpg /usr/share/keyrings/microsoft-archive-keyring.gpg
sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/usr/share/keyrings/microsoft-archive-keyring.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
apt-get update
apt-get install code # 安装VSCode
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb #下载Chrome
wget https://repo.skype.com/latest/skypeforlinux-64.deb
apt install ./google-chrome-stable_current_amd64.deb #安装Chrome
apt install ./skypeforlinux-64.deb
# Typora
wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -
add-apt-repository 'deb https://typora.io/linux ./'
apt-get update
# Typora
apt-get install typora
im-config  #设置输入法为fcitx5后注销。
```
下载vmware workstation pro
https://www.vmware.com/go/getworkstation-linux
配置hosts
sudo vim /etc/hosts
127.0.0.1 reg.code-industry.net