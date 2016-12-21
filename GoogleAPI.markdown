![GoogleAPI OAuth](http://git.moregeek.com/uploads/lin/Note/f69398899b/GoogleAPI_OAuth.png)

如果在"已授權的重新導向 URI" 欄位輸入URI值(如：http://www.andy.net/loginGoogleSuccess.php)
則在"已授權的 JavaScript 來源"就必須考慮輸入相對應的 URI
(如：http://www.andy.net 和 https://apis.google.com)
才能正常登入取得使用者資訊

***    

如果 "已授權的重新導向 URI" 和 "已授權的 JavaScript 來源" 都未設定
還是有 redirect_uri_mismatch 的錯誤
先確認在 onSuccess 事件是否有觸發回傳正確結果
並檢查 console 是否有顯示錯誤訊息