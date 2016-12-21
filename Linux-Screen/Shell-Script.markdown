```

DB_URL=192.168.1.121
DB_PORT=6379
DB_PASSWORD=
FTP_HOST=192.168.1.121
FTP_URI="\/home\/moregeek\/web"
FTP_USER=moregeek
FTP_PASSWORD=moregeek
COMPANY_ID=1
ZH_CH_MGT="http:\/\/192.168.3.205"
ZH_TH_MGT="http:\/\/192.168.3.205"
ZH_ID_MGT="http:\/\/192.168.3.205"
ZH_MY_MGT="http:\/\/192.168.3.205"
ZH_SG_MGT="http:\/\/192.168.3.205"
ZH_CH_REGION_ID=1
ZH_TH_REGION_ID=1
ZH_ID_REGION_ID=1
ZH_MY_REGION_ID=1
ZH_SG_REGION_ID=1
ZH_CH_PRODUCT_IDS=1
ZH_TH_PRODUCT_IDS=1
ZH_ID_PRODUCT_IDS=1
ZH_MY_PRODUCT_IDS=1
ZH_SG_PRODUCT_IDS=1

cat config.properties.sample | sed -e "s/@DB_URL@/$DB_URL/" | sed -e "s/@DB_PORT@/$DB_PORT/" \
							 | sed -e "s/@DB_PASSWORD@/$DB_PASSWORD/" | sed -e "s/@FTP_HOST@/$FTP_HOST/" \
							 | sed -e "s/@FTP_URI@/$FTP_URI/" | sed -e "s/@FTP_USER@/$FTP_USER/" \
							 | sed -e "s/@FTP_PASSWORD@/$FTP_PASSWORD/" \
							 | sed -e "s/@COMPANY_ID@/$COMPANY_ID/" | sed -e "s/@ZH_CH_MGT@/$ZH_CH_MGT/" \
							 | sed -e "s/@ZH_TH_MGT@/$ZH_TH_MGT/" | sed -e "s/@ZH_ID_MGT@/$ZH_ID_MGT/" \
							 | sed -e "s/@ZH_MY_MGT@/$ZH_MY_MGT/" | sed -e "s/@ZH_SG_MGT@/$ZH_SG_MGT/" \
							 | sed -e "s/@ZH_CH_REGION_ID@/$ZH_CH_REGION_ID/" | sed -e "s/@ZH_TH_REGION_ID@/$ZH_TH_REGION_ID/" \
							 | sed -e "s/@ZH_ID_REGION_ID@/$ZH_ID_REGION_ID/" | sed -e "s/@ZH_MY_REGION_ID@/$ZH_MY_REGION_ID/" \
							 | sed -e "s/@ZH_SG_REGION_ID@/$ZH_SG_REGION_ID/" | sed -e "s/@ZH_CH_PRODUCT_IDS@/$ZH_CH_PRODUCT_IDS/" \
							 | sed -e "s/@ZH_TH_PRODUCT_IDS@/$ZH_TH_PRODUCT_IDS/" | sed -e "s/@ZH_ID_PRODUCT_IDS@/$ZH_ID_PRODUCT_IDS/" \
							 | sed -e "s/@ZH_MY_PRODUCT_IDS@/$ZH_MY_PRODUCT_IDS/" | sed -e "s/@ZH_SG_PRODUCT_IDS@/$ZH_SG_PRODUCT_IDS/" \
							 > config.properties

./startup.sh

```