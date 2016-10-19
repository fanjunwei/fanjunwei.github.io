.. title: centos7安装RabbitMQ启动错误
.. slug: centos7-an-zhuang-rabbitmq-qi-dong-cuo-wu
.. date: 2016-10-19 17:11:53 UTC+08:00
.. tags: rabbitmq,centos,centos7
.. category: 
.. link: 
.. description: 
.. type: text

错误信息::

    rabbitmq-server.service - RabbitMQ broker
    Loaded: loaded (/usr/lib/systemd/system/rabbitmq-server.service; enabled; vendor preset: disabled)
    Active: failed (Result: exit-code) since 日 2016-08-28 04:36:09 EDT; 20s ago
    Process: 17876 ExecStop=/usr/lib/rabbitmq/bin/rabbitmqctl stop (code=exited, status=0/SUCCESS)
    Process: 17777 ExecStart=/usr/lib/rabbitmq/bin/rabbitmq-server (code=exited, status=1/FAILURE)
    Main PID: 17777 (code=exited, status=1/FAILURE)

    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: attempted to contact: [rabbit@10]
    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: rabbit@10:
    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: * unable to connect to epmd (port 4369) on 10: badarg (unknown POSIX error)
    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: current node details:
    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: - node name: 'rabbitmq-cli-77@10'
    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: - home dir: /var/lib/rabbitmq
    8月 28 04:36:09 10.211.55.11 rabbitmqctl[17876]: - cookie hash: 7lHQPF5Hz7+G83gtXMztYA==
    8月 28 04:36:09 10.211.55.11 systemd[1]: Failed to start RabbitMQ broker.
    8月 28 04:36:09 10.211.55.11 systemd[1]: Unit rabbitmq-server.service entered failed state.
    8月 28 04:36:09 10.211.55.11 systemd[1]: rabbitmq-server.service failed.

网上查资料发现是因为rabbitmq无法通过当前主机名解析出ip地址，所有需要修改hosts文件 ::

    #vi /etc/hosts
        127.0.0.1 localhost.localdomain   localhost  <此处加上当前主机名>


附：
+++++++++++++++++++++

centos7查看hostname和修改hostname的方法

查看使用hostname命令

修改使用 hostnamectl set-hostname NAME
