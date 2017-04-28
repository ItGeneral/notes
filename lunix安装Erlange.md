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
8:验证是否生效，命令：echo $ERL_HOME 结果:/usr/local/erlang  
