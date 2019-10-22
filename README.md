### docker构建nodejs测试服务器环境 ###

* nginx
* nodejs + npm + pm2
* mysql
* redis
* gitlab

***

#### 前提要求 ####

在机器安装并配置好了docker环境，确定 docker-compose.yml 文件中用到的端口没有被占用

#### 使用方法 ###

在docker-compose.yml所在目录下执行: `docker-compose up -d`
然后是等待(mysql镜像比较大，可能需要比较久的时间)...
完成后查看有没有 Error 提示，然后在命令行里用 `docker ps` 查看是否已经有运行

#### 补充说明 ####

建议是已经熟悉docker的开发者或者运维人员使用，具体说明以后补充

#### 注意事项 ####

mysql 下的 dbSave.sh 是定时备份任务文件，需要修改为自己的数据库名称，然后设置 crontab 定时备份