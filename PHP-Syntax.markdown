* mb_convert_encoding 轉換編碼，無法轉換的將以問號(?)顯示

# Heredoc
<code>    


$param = "World";
$test =     
<<<EOF
Hello {$param}!!!
EOF;


</code>    