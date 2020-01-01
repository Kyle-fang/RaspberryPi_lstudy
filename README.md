# RaspberryPi_study
## 树莓派身世
- 树莓派由注册于英国的慈善组织“Raspberry Pi 基金会”开发，Eben·Upton/埃·厄普顿为项目带头人。2012年3月，英国剑桥大学埃本·阿普顿（Eben Epton）正式发售世界上最小的台式机，又称卡片式电脑，外形只有信用卡大小，却具有电脑的所有基本功能，这就是Raspberry Pi电脑板，中文译名"树莓派"。这一基金会以提升学校计算机科学及相关学科的教育，让计算机变得有趣为宗旨。基金会期望这 一款电脑无论是在发展中国家还是在发达国家，会有更多的其它应用不断被开发出来，并应用到更多领域。
- **windows系统看似友好的图形化界面，把计算机真正的工作流程都隐藏在幕后，让青少年失去了进一步探索的动力**

# 获取root权限

`sudo su`

# (一)更换软件原
## 打开终端输入：
`sudo nano /etc/apt/sources.list `
## 将更改下面文本中加粗的文字：
```
deb http://**mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian**/ buster main contrib $ <br>
#Uncomment line below then 'apt-get update' to enable 'apt-get source' <br>
#deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ buster main contrib non-$ <br>
```
## 目前最新的树莓派中国大陆地区的软件源:

中国科学技术大学
Raspbian http://mirrors.ustc.edu.cn/raspbian/raspbian/

阿里云
Raspbian http://mirrors.aliyun.com/raspbian/raspbian/

清华大学
Raspbian http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/

华中科技大学
Raspbian http://mirrors.hustunique.com/raspbian/raspbian/
Arch Linux ARM http://mirrors.hustunique.com/archlinuxarm/

华南农业大学（华南用户）
Raspbian http://mirrors.scau.edu.cn/raspbian/

大连东软信息学院源（北方用户）
Raspbian http://mirrors.neusoft.edu.cn/raspbian/raspbian/

重庆大学源（中西部用户）
Raspbian http://mirrors.cqu.edu.cn/Raspbian/raspbian/

新加坡国立大学
Raspbian http://mirror.nus.edu.sg/raspbian/raspbian

## 更新软件源
`sudo apt-get upgate`
## 更新软件
`sudo apt-get upgrade`

# (二)安装中文输入法
`sudo apt-get install scim-pinyin`
   - 然后重启
      - `reboot`
   ## 树莓派安装scim-pinyin后Ctrl＋space切换不了中文输入法
   该解决方法在树莓派4B上亲测有效
- 右键点击树莓派操作界面右上输入法图标-->点击退出按钮（输入法的图标会消失）
- 打开终端输入
    - `sudo scim`
  输入法会被重启,这个时候Ctrl＋space就可以切换了
- **注意**：scim-pinyin输入法有一个BUG：
   - 必须在输入框内时，按Ctrl＋space才有效
      
# (三)解决中文名的wifi乱码和连接不上的的问题
- 若WIFI没有密码
   - ```
     network={ssid="WiFi的名称"
     key_mgmt-NONE
     }
- 若WiFi使用WEP加密
   - ```
     network={ssid="WiFi名称"
     key_mgmt=NONE
     wep_key0="WiFi密码"
     } 
- 若WiFi使用WPA／WPA2加密
   - ```
     network={ssid="WiFi名称"
     key_mgmt=WPA-PSK
     psk="WiFi密码"
     }
   

## 安装jupyter notebook
- 更新软件源
   - `apt-get update`
   - `apt-get dist-upgrade`
- 软件由Python（pip）管理， 而不是由操作系统软件管理器（APT）管理。输入以下命令，可以得到所需得要的一切。
   - `apt-get install python3-matplotlib`
   - `apt-get install python3-scipy`
- 安装jupyter
   - `pip3 install jupyter`\
- 输入以下指令，清理为了更新树莓派而下载的软件包
   - `apt-get clean`
   
   
