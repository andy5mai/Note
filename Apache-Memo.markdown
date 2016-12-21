# service apache2 restart [failed]    
試試用 root 權限執行

# 查看 apache2 套用的模組
sudo apache2ctl -M

# 套用 rewrite 模組
sudo a2enmod rewrite

# 撰寫額外的 conf
在 conf-available 裡面編輯 conf 檔(ex: remoteip.conf)    
之後套用 conf 會在 conf-enabled 建立 symbolink 連結到 conf-available 的 remoteip.conf 檔    
取消套用 conf 會將該 symbolink 連結刪除    

# 套用 conf    
a2enconf [Config Name]

# 取消套用 conf    
a2disconf [Config Name]

# 查看 apache service 狀態
systemctl status [service]    
如：systemctl status apache2.service

# 查看 apache 的 error log
/var/log/apache2/error.log

# 使用 rotatelogs 分割 ErrorLog
在 conf 中設定 ErrorLog 為 "|/usr/bin/rotatelogs /etc/apache2/logs/xxx-error_%Y%m%d 86400"
詳細設定參考 apache 官網

# 找不到 rotatelogs ?
通常會在 /usr/bin/ 底下    
還是沒有的話，試試安裝 apache2-utils    
sudo apt-get install apache2-utils