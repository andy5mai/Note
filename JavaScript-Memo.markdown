# JavaScript src 路徑    
./    指定目前的目錄    
`<script type="text/javascript" src="./a.js"></script>`

../   指定上一層的目錄    
`<script type="text/javascript" src="../a.js"></script>`   

/    根目錄    
`<script type="text/javascript" src="/a.js"></script>`

# foreach
<code>

    for(var key in XXX)    
    {    
        XXX[key]    
    }

<code>

# escape quote    
encodeURIComponent    

# 若 php 用 rawurlencode 或 urlencode
則 javascript 可用 decodeURIComponent 解回

# 設定方法執行間隔時間
var myVar = setInterval(function(){ myTimer() }, 1000);

# 取消方法執行間隔時間
clearInterval(myVar);