#  Using start-stop-daemon on CentOS
## Refer： [http://www.centoscn.com/CentOS/help/2016/1209/8270.html](http://www.centoscn.com/CentOS/help/2016/1209/8270.html)
    
```sh
    cd /tmp    
    wget http://ftp.de.debian.org/debian/pool/main/d/dpkg/dpkg_1.16.18.tar.xz    
    tar -xf dpkg_1.16.18.tar.xz       
    cd dpkg-1.16.18   
    ./configure   
    yum install gcc   # error: no C compiler
    yum install ncurses-devel -y # error: no curses library found
  
    ./configure && make
    find / -name start-stop-daemon 

    #copy到/usr/local/sbin/下。
    cp /tmp/dpkg-1.16.18/utils/start-stop-daemon /usr/local/sbin/
    
```
