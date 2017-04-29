1、将本机的文件copy到另外一台机子：`scp -r /root/tools/ root@123.249.76.119:/root/tools/`  
2、查看端口使用情况：`netstat -ntlp`    
3、解压压缩包到另一个路径 `tar -xvf /root/tools/tools/nodejs/node-v7.8.0-linux-x64.tar.xz -C /usr/local/node`    
4、建立软连接，设置成全局变量：`ln -s /usr/local/nodejs/bin/npm /usr/local/bin`     
5、安装zip,unzip命令：`yum install -y unzip zip`  
6、查看某个端口占用情况：`ps -aux | grep pid`  
7、查看所有java进程：`ps -ef | grep java`，查看tomcat进程也一样  
