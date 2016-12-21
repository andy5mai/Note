# 連線
* mysql -h {host} -u account -p {password}

# 設定檔
* /etc/mysql/my.cnf

# log 檔 (需在 my.cnf 中啟用並指定檔案位置)
* /var/log/mysql/mysql.log
* /var/log/mysql/error.log

# 啟動
* /etc/init.d/mysql start
* service mysql start

# 重啟
* service mysql restart    
若是重啟失敗，有可能是某些設定的路徑沒有權限

# 狀態
* service mysql status

# 設定 MySql 不監聽特定 host
* 修改 my.cnf 裡的 bind-address 為 0.0.0.0

# settings
https://dev.mysql.com/doc/refman/5.5/en/server-system-variables.html#sysvar_max_connections

# show variables
show variables like '%max%'

# show status
show status