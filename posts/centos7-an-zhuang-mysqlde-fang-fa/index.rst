.. title: Centos7 安装Mysql的方法
.. slug: centos7-an-zhuang-mysqlde-fang-fa
.. date: 2016-11-11 14:08:04 UTC+08:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text

Centos的mysql默认换成了MariaDB，如果只是运行::

    yum install mysql

只会安装MariaDB的客户端，不能启动服务，要执行::

    yum install mariadb-server

这样才能安装mysql的服务，启动mysql服务::

    systemctl start mariadb
    systemctl enable mariadb #开机启动


