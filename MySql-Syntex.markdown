# Alter
* alter table 'table_name' add index ('column_name');
* alter table 'table_name' drop index 'column_name';
* alter table 'table_name' auto_increment = 1;
* alter table relation3 change rel_col rel_col_name char(30)
* alter table 'table_name' add 'column_name' int unsigned not null auto_increment, add index ('column_name');

# delete
* delete from employee_login;
* delete from employee_login where ...;


# update
update free_to_play_log as a set storeId = (select storeId from machine as b where a.machineId = b.id)    
update free_to_play_log as a set distributorId = (select distributorId from store as b where a.storeId = b.id)    
update free_to_play_log as a inner join store as b set a.distributorId = b.distributorId where a.storeId = b.id

#insert
insert into users_record(`playerId`) select id from `users` where email = 'guest1@moregeek.com';