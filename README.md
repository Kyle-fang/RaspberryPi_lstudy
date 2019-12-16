# RaspberryPi_study

# (一)更换软件原
## 打开终端输入：
' sudo nano /etc/apt/sources.list '
## 将更改下面文本中加粗的文字：
'''
deb http://**mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian**/ buster main contrib $ <br>
#Uncomment line below then 'apt-get update' to enable 'apt-get source' <br>
#deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ buster main contrib non-$ <br>
'''
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
'''
sudo apt-get upgate
'''
## 更新软件
'''
sudo apt-get upgrade
'''
