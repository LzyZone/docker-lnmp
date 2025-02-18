# docker-lnmp
## 软件版本
php 7.4.33

mysql 5.7.43

nginx 1.24.0

redis 7.0.12

rabbitmq 3.12.6

elasticsearch 7.17.6

maxwell

percona-xtrabackup 2.4.28

## 操作步骤
###1.启动 php + mysql + nginx + redis

docker-compose up --build -d

###2.启动elasticsearch+kibana

cd elasticsearch

docker-compose up --build -d

###3.启动rabbitmq

cd rabbitmq

docker-compose up --build -d

###4.启动maxwell

cd maxwell

docker-compose up -d

###5.备份数据库

目录：percona-xtrabackup

####全量备份脚本
backup.sh

####增量备份脚本
backup-inc.sh

####全量恢复脚本
restore.sh

####增量恢复脚本
restore-inc.sh









