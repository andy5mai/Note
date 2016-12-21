# 若 phpinfo() 顯示的 session.save_path 是 "no value"，可用 session_save_path() 查看    
通常 linux 會是在 /var/lib/php/sessions 底下    

# 系統刪除 session 的參考因素有：
1. session.gc_probability 
2. session.gc_divisor 
3. session.gc_maxlifetime    
gc_probability 和 gc_divisor 是搭配使用的，即 gc_probability/gc_divisor，假設為 1/1000 則表示有千分之一的機會在接收 request 的時候刪除 session。gc_maxlifetime 是設定用來判斷是否為可回收刪除的生命週期時間，單位為秒。    

# php 可能也會在 crontab 設定刪除 session 的工作
路徑可查看 /etc/cron.d/php 裡的工作設定
(是否 php 就是靠這個 crontab 來刪除過期的 session?)