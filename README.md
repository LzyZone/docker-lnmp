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
### 1.启动 php + mysql + nginx + redis
``` shell script
docker-compose up --build -d
```

### 2.启动elasticsearch+kibana
``` shell script
cd elasticsearch
docker-compose up --build -d
```

### 3.启动rabbitmq
``` shell script
cd rabbitmq
docker-compose up --build -d
```

### 4.启动maxwell
``` shell script
cd maxwell
docker-compose up -d
```

### 5.备份数据库

目录：percona-xtrabackup

#### 全量备份脚本
``` shell script
backup.sh
```

#### 增量备份脚本
``` shell script
backup-inc.sh
```

#### 全量恢复脚本
``` shell script
restore.sh
```

#### 增量恢复脚本
``` shell script
restore-inc.sh
```










