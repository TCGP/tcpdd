# tcpdd  
##record tcpdump raw data  

##basic:  
tcpdd port[num] dir[inout|in|out] infterface[any|ethx|ensx] pef[string]  
  
every record is 1 hour [ *on the hour ], it's design for crontab running like  
0 * * * * tcpdd 80 in eth0 mydump  
  
##how to use:  
git clone https://github.com/ntulp/tcpdd.git  
cd tcpdd  
chmod a+x tcpdd  
mv tcpdd /usr/sbin/  
  
crontab -e  
0 * * * * tcpdd 80 in eth0 mydump

