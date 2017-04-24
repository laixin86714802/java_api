# java_code
java接收处理请求, 存入redis, 每小时写入linux

| 程序名 | 作用 | 部署 | 推送 | 注意 |
|----|----|----|----|----|
| bigeate | 将stat.js和monitor.js推送的数据存入redis | 部署在141-144的/data/apps/tomcat7/webapps/bigeater目录下 | 数据推送到143下的redis数据库 | redis有两个端口，6379和6380。密码均为admin。|
| ashman | 将存入redis的数据汇聚成文件，每小时生成一个文件 | 部署在142上 | 生成的文件放在/data/pccontrail和/data/mcontrail | |
| thirdparty | 将ad.js送的数据存入redis | 部署在147-149的/opt/server/tomcat7/webapps/thirdparty目录下 | 数据推送到149下的redis数据库 | redis端口为6381。密码为admin。|