# 瀏覽器基於資料安全的原則，為防止惡意程式碼傳送資料到其它站台，預設都會禁止跨網域連線

# 跨網域資料傳送的方法
* Form submit    
  即利用 iframe 的 src 偷傳資料
* JSONP
* W3C - CORS (Cross-Origin Resource Sharing)    
  在發送跨網域 Request 之前會先發出一個 OPTION Request 來詢問目的網站是否接受跨網域的 Request，如果接受才會發送真正的 Request    
header('Access-Control-Allow-Origin: http://base.com');  --> `定義了允許從哪個網域發 Request 過來`     
header('Access-Control-Allow-Methods: GET, POST, PUT, DELETE, OPTIONS');    --> `允許使用哪幾種 HTTP Methods`    
header('Access-Control-Allow-Headers: X-Requested-With, Content-Type, Accept');  --> `允許夾帶哪些 Headers`    
    
每次都用 OPTION 詢問有些浪費資源，其實可以透過 Access-Control-Max-Age 這個 Header 來指定規則的有效期限 (類似 Cookie 的機制)，在這個有效時間內瀏覽器就會直接發送而不會一一詢問了，提昇了不少效率

```   
123456
789
123
78945
```
