# ToDo
* [List](http://git.moregeek.com/lin/Note/wikis/Work/ToDo-List)

***

# Social
* [Troble](http://git.moregeek.com/lin/Note/wikis/Work/Social-Troble)

***

# UTK
* [Request](http://git.moregeek.com/lin/Note/wikis/Work/UTK-Request)

***

# HOU
* [Request](http://git.moregeek.com/lin/Note/wikis/Work/HOU-Request)
* [Room](http://git.moregeek.com/lin/Note/wikis/Work/HOU-Room)

***

# MGT
* [List](http://git.moregeek.com/lin/Note/wikis/Work/MGT-List)
* [Troble](http://git.moregeek.com/lin/Note/wikis/Work/MGT-Troble)
* i18n 暫時未做 H_page.php, page_link.php

***

# MBR
* [List](http://git.moregeek.com/lin/Note/wikis/Work/MBR-List)
* [Troble](http://git.moregeek.com/lin/Note/wikis/Work/MBR-Troble)
* [1758](http://git.moregeek.com/lin/Note/wikis/Work/MBR-1758)

# UTK_OR
* [sql](http://git.moregeek.com/lin/Note/wikis/Work/UTK_OR-sql)

# Report
* 查詢消耗金幣排名    

```

set @start_time = '2015-11-11 00:00:00';
set @end_time = '2015-11-11 14:19:00';        
SELECT DISTINCT(a.total), member_sn AS member_sn FROM (SELECT SUM(data4) as total, member_sn FROM 19_8_money_update  WHERE date_format(data1,"%Y-%m-%d %H:%i:%s") <=  @end_time AND date_format(data1,"%Y-%m-%d %H:%i:%s") >=  @start_time AND CAST(data3 AS SIGNED)  >= 1001 GROUP BY member_sn ORDER BY total desc) AS a LIMIT 0,8

```    

* 查詢成員消耗金幣數量    

```
set @start_time = '2015-11-11 00:00:00';
set @end_time = '2015-11-11 14:19:00';
set @member_sn = 300796;
select * from 19_8_money_update WHERE date_format(data1,"%Y-%m-%d %H:%i:%s") <=  @end_time AND date_format(data1,"%Y-%m-%d %H:%i:%s") >=  @start_time AND CAST(data3 AS SIGNED)  >= 1001 and member_sn = @member_sn
```    

# Log
* step-1 api ... 有 consume api, game log api, 可分不同 server    
* step-2 log queue(mysql)，專門用來收集 game log api，每五分鐘往 step 3 送，為的是消化大量送來的 game log    
* step-3 log db 當初設計為可拆, action 定義不同型態要往哪裡丟，可以拆開也可以合併    

* mgg_log_action 有兩種型態    
type 為 1 是 game log，type 為 2 是 consume log

log action    
log server

* 90.91.92 game log api share mem key
92 是 mgg_log_server    
93.94 consume log api, game log api cache

* 因為 game log 的 db 和 consume 的 db 可能不是同一台，為了要撈報表資料，需要將 consume 的資料定時 sync 到 game log 的 db , 這樣報表才找得到資料