# 設定 CORS   
  在 Virtual Host 設定加入 Header always set Access-Control-Allow-Origin "*"
  如 ：    
  <code>
  <VirtualHost *:80>
    DocumentRoot e:/svn/php_old
    ServerName www.phpold.net
    Header always set Access-Control-Allow-Origin "*"
	
	<Directory "e:/svn/php_old/">
		Options FollowSymLinks
		AllowOverride none
		Require all granted
	</Directory>
    
    ErrorLog logs/www.phpold.net-error_log
    CustomLog logs/www.phpold.net-access_log common
  </VirtualHost>
  </code>

