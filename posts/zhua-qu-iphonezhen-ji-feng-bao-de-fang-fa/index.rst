.. title: 抓取iPhone真机封包的方法
.. slug: zhua-qu-iphonezhen-ji-feng-bao-de-fang-fa
.. date: 2015-10-4 22:55:00 UTC+08:00
.. tags: ios,抓包
.. category: 
.. link: 
.. description: 
.. type: text


iOS 5后，apple引入了RVI remote virtual interface的特性，它只需要将iOS设备使用USB数据线连接到mac上，然后使用rvictl工具以iOS设备的UDID为参数在Mac中建立一个虚拟网络接口rvi，就可以在mac设备上使用tcpdump，wireshark等工具对创建的接口进行抓包分析了。

iOS APP网络分析之rvictl（可以捕捉除了Wifi以外的网络类型） - 碳基体 - 碳基体

这种流量分析方法，是直接捕捉的iOS设备上的网络流量，因此无论是wifi还是2G/3G等其他网络类型都可以捕捉到，一根USB数据线就搞定了，不需要苛刻的要求PC与iOS设备处于同一个网段，或必须越狱等局限了。

下面介绍使用方法

1. 使用USB数据线将iOS设备连接到MAC上
2. 获得iOS设备的UDID，可以使用iTools查看，也可以使用Xcode的Organizer工具查看
3. 创建RVI接口::

    $rvictl -s <UDID>

    RVI虚拟接口的命令规则可为rvi0，rvi1，。。。,创建后可以使用以下命令查看是否创建成功

    $ifconfig rvi0


4. 在mac上用抓包工具wireshark或tcpdump等工具抓包分析::

    $sudo tcpdump -i rvi0 -n -vv

    iOS APP网络分析之rvictl（可以捕捉除了Wifi以外的网络类型） - 碳基体 - 碳基体

5. 分析结束后，移除创建的RVI接口::

    $rvictl -x <UDID>

