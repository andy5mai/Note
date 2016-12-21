# 寫不進 log ?
* 檢查 php.ini 的 log_errors、error_reporting 和 error_log 設定
* 檢查該資料夾的權限

# 未設定 error_log 的路徑，以 php 執行檔直接執行 php 檔
* 若有設定 error_reporting，則 log 應該在執行當下的資料夾中

# curl 的 cookie 沒寫進去
* 檢查是否寫到 apache 的資料夾底下去了

# curl 要注意 CURLOPT_POST 和 CURLOPT_POSTFIELDS 的設置順序
* 先設 CURLOPT_POST 再設 CURLOPT_POSTFIELDS)，否則可能導致 CURLOPT_POSTFIELDS 的值送不出去