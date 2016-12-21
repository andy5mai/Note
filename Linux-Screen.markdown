# [Screen](http://git.moregeek.com/lin/Note/wikis/Linux-Screen/Screen)

***

# [Shell-Script](http://git.moregeek.com/lin/Note/wikis/Linux-Screen/Shell-Script)

***

# 修改時區   
  sudo dpkg-reconfigure tzdata

# 統計資料夾大小   
  du -h --max-depth=1

# 查看含有 mysql 關鍵字的 process
ps -ef | grep mysql

# 複製資料夾中所有的東西
cp -r sources destination

# tar
-c 打包一個 tar 檔案    
-x 解開一個 tar 檔案    
-t 檢視 tar 檔案的內容    
-z 使用 gzip 壓縮    
-v 顯示建立 tar 檔案的過程    
-P 使用絕對路徑    
-f 指定 tar 檔案的檔案名稱。此參數的後面要接檔案名稱，因此要注意參數的順序 (通常是把 f 參數寫在最後一個，或者是與其它參數拆開使用)    

tar -cf 檔案名稱.tgz 來源檔案    
tar -cf 20160407.tar *

# 建立 Symbolic Link
ln -s [來源路徑] [目的路徑]

# 改變目錄資料夾底下所有權限
chmod -R 777 *

# 改變目錄資料夾擁有者(包含所有檔案)
chown -R [群組]:[使用者] [資料夾名稱]

# 找出 cron 並執行
> which cron    
>> /usr/sbin/cron    

> /usr/sbin/cron    

# 以現在的使用者執行 crontab
crontab -e

# 指定執行的使用者並寫在系統層級的 cron
sudo vim /etc/crontab

# vim 時使用 sudo 權限存檔
:w !sudo tee %

# 查看 service 狀態
systemctl status [service]    
如：systemctl status apache2.service

# 沒有 telnet 時，就試試 nc 吧!
nc -v {host} [port]    
-v 參數可以在連線成功後輸入指令來和主機互動    
e.g. nc -v 127.0.0.1 11211

# 查看 syslog
/var/log/syslog

# 取消 限制
ulimit -c unlimited