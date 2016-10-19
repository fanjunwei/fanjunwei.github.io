.. title: 为 Mac Terminal 设置代理
.. slug: wei-mac-terminal-she-zhi-dai-li
.. date: 2015-5-27 10:54:00 UTC+08:00
.. tags: mac,代理
.. category: 
.. link: 
.. description: 
.. type: text

使用brew安装软件时,brew并不走系统设置的代理,下面介绍一种方法

Install & Config::

    step1. brew install proxychains-ng
    step2. modify config file(/usr/local/Cellar/proxychains-ng/4.7/etc/proxychains.conf), add or modify: socks5 127.0.0.1 23333
    PS: use your own local port to replace 23333

Usage::

    proxychains4 ping facebook.com
    proxychains4 -q pip install shadowsocks


