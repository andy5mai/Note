# 2015/09/09 DMM 同步清單
/PHP/MG/test/MBR/andy/loginMobile.php    
/PHP/MG/test/MBR/andy/mobile_login.php    
/PHP/MG/test/MBR/classes/user/member/member_register.php    
/PHP/MG/test/MBR/classes/user/third/third_login.php     
/PHP/MG/test/MBR/includes/init.php    
/PHP/MG/test/MBR/index.php    
/PHP/MG/test/MBR/mobile/stages/api/mobile/mobile_login.php    

insert into mgg_third_switch set id = 'DMM', name='DMM', proc_path='', region='', third_type='DMM', channel='all', mobile_api='Y'    
insert into mgg_third_switch_project set third_sn='12', product_id='1', region_id='1'

# 2015/10/13 1758測試 同步清單
* insert into mgg_payment_type set sort_no = 0, name = 'WEB直儲-1758', param = 'web_direc_store_1758', url_path = null, class = 'o'
, pic = '', hover_pic = '', small_pic = '', currency = '1', region = '1', is_need_pdt_code = 0
, channel = 'web', is_enabled = 1;

* insert into mgg_payment_product set region = 1, product_id = 3, payment_type = 28, name = '直儲金幣', description = '直儲金幣'
, point = 0, money = 0, currency_id = 1, product_code = '', product_type = 1, is_enabled = 1;

* insert into mgg_payment_product_item set sn = 0, product_sn = 28, item_id = '', item_quan = 0, item_note = 'HOI 金幣'