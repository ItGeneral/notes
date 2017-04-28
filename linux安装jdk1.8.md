1：下载linux的jdk1.8，下载地址：http://pan.baidu.com/s/1hrRleXe  
2：在usr/local目录下,将下载的jdk拷贝到java目录下；cp jdk地址 /usr/local  
3：解压jdk，tar -zxvf /usr/local/jdk-8u40-linux-x64.gz，得到jdk1.8.0_40文件，解压完成后将压缩包删除了  
4：编辑配置文件，配置环境变量：执行命令vim /etc/profile，在最后添加如下内容  
JAVA_HOME=/usr/local/jdk1.8.0_40 CLASSPATH=$JAVA_HOME/lib   
PATH=$PATH:$JAVA_HOME/bin   
export PATH JAVA_HOME CLASSPATH    
5：使配置立即生效：source /etc/profile  
6：查看是否安装成功：java -version  
