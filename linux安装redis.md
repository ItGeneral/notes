1：下载 `wget https://github.com/antirez/redis/archive/4.0-rc2.tar.gz`  
2：解压到usr/local `tar -xvf 4.0-rc2.tar.gz -C /usr/local`  
3：cd到redis根目录进行测试 `make test`，`make PREFIX=/usr/local/redis install`，`mkdir -p /usr/local/redis/etc`, `cp redis.conf /usr/local/redis/etc/`    
4：修改redis.conf配置， daemonize 改成yes ， 让reids在后台运行  
5：启动服务端redis：`/usr/local/redis/bin/redis-server /usr/local/redis/etc/redis.conf`  
6：启动客户端redis：`/usr/local/redis/bin/redis-cli`  
7:测试是否安装成功：`set test helloworld`,   `get test` ,结果：“helloworld”

