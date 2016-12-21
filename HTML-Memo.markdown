# Cross-Origin Resource Sharing (CORS) 跨來源資源共享
https://developer.mozilla.org/zh-TW/docs/HTTP/Access_control_CORS    
發出請求所在網域不同於請求所指向之網域的HTTP請求    
用XMLHttpRequest物件所發出的請求受限於同源政策(same-origin policy)，只能發送HTTP請求到和其所來自的相同的網域    
## 標頭設定
header('Access-Control-Allow-Origin: http://arunranga.com');    
header('Access-Control-Allow-Methods: POST, GET, OPTIONS');    
header('Access-Control-Allow-Headers: X-PINGARUNER');    
header('Access-Control-Max-Age: 1728000');    

## XSS (Cross-site scripting)
很多時候可以使用HTTP頭指定內容的類型，使得輸出的內容避免被作為HTML解析。如在PHP語言中使用以下代碼：
`
<?php
   header('Content-Type: text/javascript; charset=utf-8');
?>
`