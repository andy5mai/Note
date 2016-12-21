# 2015-09-25
1. 192.168.3.205 送信有問題    
  Missing argument 3 for post_curl(), called in /var/www/MGT/stages/mgg/post/gift_exchange_post.php on line 86 and defined in /var/www/MGT/functions/H_function.php on line 66    
  Missing argument 4 for post_curl(), called in /var/www/MGT/stages/mgg/post/gift_exchange_post.php on line 86 and defined in /var/www/MGT/functions/H_function.php on line 66    
  Missing argument 5 for post_curl(), called in /var/www/MGT/stages/mgg/post/gift_exchange_post.php on line 86 and defined in /var/www/MGT/functions/H_function.php on line 66    
 Undefined variable: cookie in /var/www/MGT/functions/H_function.php on line 80    
 Undefined variable: cookie in /var/www/MGT/functions/H_function.php on line 88    
 Undefined variable: referer_url in /var/www/MGT/functions/H_function.php on line 94    
 Undefined variable: proxy in /var/www/MGT/functions/H_function.php on line 104    
 Undefined index: project in /var/www/MGT/includes/setting_server_ip.php on line 13    
 Undefined index: project in /var/www/MGT/includes/setting_server_ip.php on line 14    
 Undefined index: pwd in /var/www/MGT/stages/api/post/mail.php on line 7    
 Array to string conversion in /var/www/MGT/stages/api/post/mail.php on line 13    
 Array to string conversion in /var/www/MGT/stages/api/post/mail.php on line 13    
 Array to string conversion in /var/www/MGT/stages/api/post/mail.php on line 13    
 Undefined index: pwd in /var/www/MGT/stages/api/post/mail.php on line 24    
 Undefined index: privateusers in /var/www/MGT/stages/api/post/mail.php on line 28    
 Undefined index: CONTENT_TYPE in /var/www/MGT/stages/api/post/mail.php on line 71    
 Undefined index: MESSAGE_TYPE in /var/www/MGT/stages/api/post/mail.php on line 73    
 Undefined index: debug in /var/www/MGT/stages/api/core/msg.php on line 32    
 Undefined index: START_TIME in /var/www/MGT/classes/data_source/MTUMail.php on line 136    
 Undefined index: DURATION in /var/www/MGT/classes/data_source/MTUMail.php on line 137    
 Undefined index: LIFE_CYCLE in /var/www/MGT/classes/data_source/MTUMail.php on line 138    
Fatal error:  Access to undeclared static property: TypeInfo::$shortsType in /var/www/MGT/classes/data_source/NetUtil.php on line 671    

2. 192.168.3.205 上面的 MTUMail.php 相關(TypeInfo.php, NetUtil.php 等) 疑似為舊的未更新

3. 192.168.3.205 的 stages\bridge\project_create\project_create_step3.php 在處理 mgg_log_action_json_field_map[$m] 時有問題，是 json_decode 之後的東西，看一下怎麼處理    
Invalid argument supplied for foreach() in /var/www/MGT/stages/bridge/project_create/project_create_step3.php on line 132

4. 1758 正式和測試的 game_log 設定不同，正式不可讓 is_approved, is_rejected, is_send, approval_status, is_deleted 為 null, 並且需有預設值

# 2015-11-20
1. LOT 在 MGT 送信會卡在 mail.php 的 redis member 檢查機制上，內測已修改，記得修改外測