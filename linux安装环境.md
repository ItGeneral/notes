一、linux安装jdk1.8
1：下载linux的jdk1.8，下载地址：`http://pan.baidu.com/s/1hrRleXe`
2：在usr/local目录下,将下载的jdk拷贝到`java`目录下；`cp jdk地址 /usr/local`
3：解压jdk，`tar -zxvf /usr/local/jdk-8u40-linux-x64.gz`，得到jdk1.8.0_40文件，解压完成后将压缩包删除了
4：编辑配置文件，配置环境变量：执行命令`vim /etc/profile`，在最后添加如下内容
`JAVA_HOME=/usr/local/jdk1.8.0_40
CLASSPATH=$JAVA_HOME/lib
PATH=$PATH:$JAVA_HOME/bin
export PATH JAVA_HOME CLASSPATH`
5：使配置立即生效：`source /etc/profile`
6：查看是否安装成功：`java -version`

二、安装tomcat
1：下载apache-tomcat-8.5.12.tar.gz，下载地址：``
2：将下载好的tomcat压缩包拷贝到usr/local目录下，`cp tomcat地址 /usr/local`
3：解压tomcat，`tar -zxvf /usr/local/apache-tomcat-8.5.12.tar.gz`，解压完成后得到apache-tomcat-8.5.12文件夹，解压完后删除压缩包
4：启动tomcat，cd 到 /usr/local目录下，执行命令` ./startup.sh `启动tomcat
5：启动完成后，访问链接`http://ip地址:8080`看看结果。


三、安装Erlange
1：yum -y install make gcc gcc-c++ kernel-devel m4 ncurses-devel openssl-devel（如果已经安装了这些就不用安装）
2：wget http://www.erlang.org/download/otp_src_R15B.tar.gz
3：tar xfvz otp_src_R15B.tar.gz
4：cd otp_src_R15B/
5：./configure --prefix=/usr/local/erlange
6：make && make install
7：添加环境配置 vim /etc/profile
ERL_HOME=/usr/local/erlang  
PATH=$ERL_HOME/bin:$PATH  
export ERL_HOME PATH  
8:验证是否生效，命令：`echo $ERL_HOME` 结果:`/usr/local/erlang`

四、安装rabbitmq
1：wget http://www.rabbitmq.com/releases/rabbitmq-server/v3.6.9/rabbitmq-server-3.6.9-1.el6.noarch.rpm
2：去依赖安装，`rpm -i --nodeps rabbitmq-server-3.6.9-1.el6.noarch.rpm`
3：启动rabbitmq，并验证启动情况 `rabbitmq-server --detached &ps aux |grep rabbitmq`
4：以服务的方式启动，`service rabbitmq-server start`
5：


五、安装nodejs
1：下载最新版本的nodejs压缩包(已经编译过)，`wget https://nodejs.org/dist/latest/node-v7.8.0-linux-x64.tar.xz`  
2：解压，`tar -xvf node-v7.8.0-linux-x64.tar.xz`  
3：移动文件（相当于重命名），`mv node-v7.8.0-linux-x64/ nodejs`  
4：将node和npm建立软连接设置成全局变量   
`ln -s /usr/local/nodejs/bin/node /usr/local/bin`  
`ln -s /usr/local/nodejs/bin/npm /usr/local/bin`
5：检验是否成功 `node -v`, `npm -v`


查看端口使用情况：netstat -ntlp
