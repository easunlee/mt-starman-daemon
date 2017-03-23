#  安装 mt-starman-daemon 简单教程
## 参考教程： [http://www.centoscn.com/CentOS/help/2016/1209/8270.html](http://www.centoscn.com/CentOS/help/2016/1209/8270.html)
    
```sh
    cd /tmp  #切换到tmp目录，习惯而已     
    wget http://ftp.de.debian.org/debian/pool/main/d/dpkg/dpkg_1.16.18.tar.xz    
    tar -xf dpkg_1.16.18.tar.xz       
    cd dpkg-1.16.18   #注意，原教程有错    
    ./configure   
    yum install gcc   #如果报告没有编译器 
    yum install ncurses-devel -y # 如果报错: no curses library found
  
    ./configure && make
    find / -name start-stop-daemon # 查看start-stop-daemon位置

    #copy到/usr/local/sbin/下。
    cp /tmp/dpkg-1.16.18/utils/start-stop-daemon /usr/local/sbin/
    
```
