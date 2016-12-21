### 2015/09/08

* 可能還要再追加一個 userType (付費後不是 "staff")
   1. 考慮是否紀錄 userType 整個從頭到尾的過程，可以覆蓋嗎?
   2. log 都是怎麼撈的?

### 2015/09

* [2015/8/27 下午 05:59:20] nothingstopsme: 預計mobile_login_dmm會傳的參數有  

+ action = mobile_login_dmm
+ id
+ product_id
+ region_id
+ displayName
+ birthday
+ gender
+ special_code
+ confirm_code = MD5(region_id + "|" + id + "|" + displayName + "|" + product_id + "|" + special_code)
+ mobile_platform  

那個mobile_platform就照原本mobin_login_fb的值之設定規則
然後access_token的部分 看起來DMM的SDK把它包起來了 不希望外部去取用
所以就先不傳啦  

* [2015/8/27 下午 06:05:42 | 已編輯 下午 06:05:46] nothingstopsme: 有需要知道每個值的type嗎?
* [2015/8/27 下午 06:06:27] Robetar: 內部協調中
* [2015/8/27 下午 06:06:27] Robetar: :D
* [2015/8/27 下午 06:07:10] Anna Chen: 應該是不需要@@
* [2015/8/27 下午 06:07:39] nothingstopsme: 好喔
* [2015/8/27 下午 06:07:42] Terrence_奉彥 Andy: displayName 是對應到原來 FB api 的 name 嗎?
* [2015/8/27 下午 06:08:19] nothingstopsme: 對 但是dmm其實還有一個叫nickName的東西