DingDing.py是主要功能，其他test都是不同形式的调用test.py是直接调用，test_timer.py加入了计划任务，test_wx使用加入计划任务和微信通知
基本参数配置在dingding.cfg
V1仅支持微信给朋友发通知
V2支持给自己文件助手通知
V3操作指令在配置文件定义


1，手机需要root，并打开 开发者模式，连接USB后传输协议选择MTP

2，需要安装adb，下载地址：https://adb.clockworkmod.com/
把ADB路径加入dingding.cfg中，如
C:\Program Files (x86)\ClockworkMod\Universal Adb Driver
安装完成后，连上USB输入adb devices可以看到连接的手机

3，手机上坐标定位需要自己改，参数在dingding.cfg
截屏
运行screen_cap.exe，系统会把截图存到程序同一目录下
用mspaint打开图片,用光标定位按键的位置，详见图片sample01和sample02

4，这里没有考虑手机加密码的情况，所以解锁密码要关掉，要处理自动输入密码原理是一样的。

5，代码调试时候把点击打卡按钮注释了，只print了操作，需要改回来才能打卡

6,节假日已经爬去到本地calendar.jason了，只有2019年所有的节假日，以后年底前需要，再跑一遍calendar_spider.exe，指令calendar_spider.exe 2019, 2020年则为calendar_spider.exe 2020

7,微信只支持发500k以下的图片，格式必须png。如果截图太大发送会失败.如果可以考虑自己做个压缩，或者换成邮件、QQ等方式通知
