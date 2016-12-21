//建立資料表    

CREATE TABLE IF NOT EXISTS `plugin_or_rating` (
  `sn` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `product_id` int(11) NOT NULL,
  `region_id` int(11) NOT NULL,
  `is_enabled` tinyint(1) UNSIGNED NOT NULL DEFAULT '0',
  PRIMARY KEY (`sn`),
  KEY `idx_pid_rid` (`product_id`,`region_id`)
) ENGINE=MyISAM  DEFAULT CHARSET=utf8;
    
//insert a new record    
INSERT INTO `plugin_or_rating` (`sn`, `product_id`, `region_id`, `is_enabled`) VALUES
(1, 1, 1, 1)
