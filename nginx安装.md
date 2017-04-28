## nginx 安装
1，下载nginx 到 /root/tools/nginx 目录：wget http://nginx.org/download/nginx-1.10.3.tar.gz  
2，移动：cp nginx-1.10.3.tar.gz /usr/local/  
3，解压：tar -xf nginx-1.10.3.tar.gz  
4，删除：rm -rf nginx-1.10.3.tar.gz  
5，cd nginx-1.10.3 执行 ./configure   
   (a)若报错：./configure: error: C compiler cc is not found ，   
   则需要先执行：yum -y install gcc gcc-c++ autoconf automake make   
   (b)若报错：./configure: error: the HTTP rewrite module requires the PCRE library.   
   则需要执行：yum -y install pcre-devel  
   (c) 报错：./configure: error: the HTTP gzip module requires the zlib library.  
   执行：yum install -y zlib-devel  
   执行：./configure  
     
6, make  
7, sudo make install  
8, 执行完毕后， nginx 即安装到 /usr/local/nginx 目录  
9,启动： /usr/local/nginx/sbin/nginx  
10，访问 http://123.206.103.107/ 即可正常访问nginx首页。  
11，修改配置 /usr/local/nginx/conf/nginx.conf 和 新增配置 /usr/local/nginx/conf/helloword.conf  
12, /usr/local/nginx/sbin/nginx -t  # 测试nginx 配置是否成功  
13，/usr/local/nginx/sbin/nginx -s reload #重启  
14, http://123.206.103.107:800/  即可成功访问 (因为这里没有使用域名，所以就只是测试了修改端口号)  

按上述步骤配置后， 访问 http://123.206.103.107:800/ 和 http://123.206.103.107:8080/  均可以访问tomcat。
区别在于， 前者通过nginx反向代理， 后者直接访问  
