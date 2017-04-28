1：下载最新版本的nodejs压缩包(已经编译过)，wget https://nodejs.org/dist/latest/node-v7.8.0-linux-x64.tar.xz  
2：解压，tar -xvf node-v7.8.0-linux-x64.tar.xz  
3：移动文件（相当于重命名），mv node-v7.8.0-linux-x64/ nodejs  
4：将node和npm建立软连接设置成全局变量  
ln -s /usr/local/nodejs/bin/node /usr/local/bin  
ln -s /usr/local/nodejs/bin/npm /usr/local/bin 5：检验是否成功 node -v, npm -v  
