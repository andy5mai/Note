# index.php

*  includes / init.php
*  includes / init_stage.php
  + $PHD['STAGE']['NAME'] in ('eip', 'bs', 'bss', 'bridge')  

            1. includes / check_perm.php
            2. includes / common_use.php

*  includes / setting_server_ip.php
*  includes / menu_control.php
*  includes / run_module.php
  +  templates / html_header.php
      	1.  $PHD['STAGE']['NAME'] == 'bs'
          *  /bs/$PHD['STAGE']['PARAM']['PRODUCT_ID']/$PHD['STAGE']['PARAM']['REGION_ID']/issue/ajax_tips  

                    1.  business/issue/main_load.php
        2.  top_menu.php
