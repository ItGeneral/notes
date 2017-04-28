1：wget http://www.rabbitmq.com/releases/rabbitmq-server/v3.6.9/rabbitmq-server-3.6.9-1.el6.noarch.rpm
2：去依赖安装，rpm -i --nodeps rabbitmq-server-3.6.9-1.el6.noarch.rpm
3：启动rabbitmq，并验证启动情况 rabbitmq-server --detached &ps aux |grep rabbitmq
4：以服务的方式启动，service rabbitmq-server start
