# RaspberryPi_study

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


