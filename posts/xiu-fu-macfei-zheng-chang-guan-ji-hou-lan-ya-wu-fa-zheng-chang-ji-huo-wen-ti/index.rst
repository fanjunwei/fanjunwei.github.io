.. title: 修复Mac非正常关机后蓝牙无法正常激活问题
.. slug: xiu-fu-macfei-zheng-chang-guan-ji-hou-lan-ya-wu-fa-zheng-chang-ji-huo-wen-ti
.. date: 2016-12-26 09:44:49 UTC+08:00
.. tags: mac,蓝牙
.. category: 
.. link: 
.. description: 
.. type: text

今天来到公司发现蓝牙键盘连接不上，重启Mac后，发现蓝牙干脆显示蓝牙不用，幸亏在论坛找到了相关的解决方法。::

    1、关机；
    2、同时按：shift+control+option+power，此时机器不会启动；
    3、等5秒（自己数）；
    4、按power，然后紧接着同时按option+command+p+r ，等苹果机器响4声开机声音后松手
    5、蓝牙菜单ok。


经过网上查询::

    Shift-Control-Option-Power 组合键来重置电源管理单元；
    重新启动时按住option+command+p+r，听见4声哗哗声后，放开按键。系统NVRAM重置恢复出厂设置

来源于：http://bbs.feng.com/read-htm-tid-499482.html