ALTER TABLE `mgg_payment_type` CHANGE COLUMN `class` `class` ENUM('p','c','m','t') NULL DEFAULT NULL COMMENT 'p:實體卡，c:信用卡，m:小額付款，t:會員點數' AFTER `url_path`;

# MyCard    
update mgg_payment_type set param = 'MyCard', url_path = '/payment/softworld/mycard/payment_path', pic = '/images/pay/mycard_ingame.png', hover_pic = '/images/pay/mycard_ingame.png', small_pic = '/images/pay/mycard.png' where name = 'MyCard';

insert into mgg_payment_type set sn = 25, sort_no = 0, name = 'MyCard_Billing', param = 'MyCard', url_path = '/payment/softworld/mycard/payment_path', class = 'm', pic = '/images/pay/mycard_billing.png', hover_pic = '/images/pay/mycard_billing.png', small_pic = '/images/pay/mycard.png', currency = '1',	region = '1', is_need_pdt_code = 0,	channel = 'web', is_enabled = 1;

insert into mgg_payment_type set sn = 26, sort_no = 0, name = 'MyCard_Point', param = 'MyCard', url_path = '/payment/softworld/mycard/payment_path', class = 't', pic = '/images/pay/mycard_point.png', hover_pic = '/images/pay/mycard_point.png', small_pic = '/images/pay/mycard.png', currency = '1', region = '1', is_need_pdt_code = 0, channel = 'web', is_enabled = 1;

# tcb-alipay 合庫支付寶
insert into mgg_payment_type set sn = 28, sort_no = 0, name = '合庫支付寶', param = 'TCB_Alipay', url_path = '/payment/tcb_alipay/express/payment_product', class = 'm', pic = '/images/pay/alipay.png', hover_pic = '/images/pay/alipay.png', small_pic = '/images/pay/alipay.png', currency = '1', region = '1', is_need_pdt_code = 0, channel = 'web', is_enabled = 1;