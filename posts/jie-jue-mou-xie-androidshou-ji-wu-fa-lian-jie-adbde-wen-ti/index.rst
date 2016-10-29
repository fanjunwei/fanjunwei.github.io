.. title: 解决某些Android手机无法连接adb的问题
.. slug: jie-jue-mou-xie-androidshou-ji-wu-fa-lian-jie-adbde-wen-ti
.. date: 2015-4-21 12:05:00 UTC+08:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text


以mac系统为例

首先执行::

    system_profiler SPUSBDataType

查看当前usb设备

以魅族mx4为例,找到以下内容::

                MX4:

                  Product ID: 0x0c02
                  Vendor ID: 0x2a45


记录下Product ID,然后执行::

    echo 0x0c02 >> ~/.android/adb_usb.ini


将Product ID加入到~/.android/adb_usb.ini文件中
