# 送出 get 卻收到 Request format is invalid: multipart/form-data; boundary=
* 試試不要設定 CURLOPT_POSTFIELDS

# 送出卻什麼都沒有
* 印出 curl_errno，若是 60，試試設定 CURLOPT_SSL_VERIFYPEER 為 false
* 印出 curl_errno，若是 35，試試設定 CURLOPT_SSL_VERIFYPEER 為 false 並注意 PORT 是否正確(SSL 為 443)

# 找個時間參考以下網頁弄個較漂亮的 base curl 吧...
* http://codex.wiki/post/162929-318

# 設定了 CURLOPT_COOKIEJAR 卻發現 cookie 寫不進去?
* 查看所在資料夾權限，可能寫在 Apache 底下
* 可能是 server 的 cookieDomain 設錯，導致無法寫入