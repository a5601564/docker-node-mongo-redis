docker-compose -f docker-compose-dev.yml up


docker-compose -f docker-mongodb.yml up

ports:
 
- "80:80" # 绑定容器的80端口到主机的80端口
 
- "9000:8080" # 绑定容器的8080端口到主机的9000端口
 
- "443" # 绑定容器的443端口到主机的任意端口，容器启动时随机分配绑定的主机端口号


# scrapy_demo
爬虫集合


一. 新建项目(scrapy startproject)
在开始爬取之前，必须创建一个新的Scrapy项目。进入自定义的项目目录中，运行下列命令：

scrapy startproject mySpider


完成 翻页 增量

# 强制跳过错误
cat requirements.txt | xargs -n 1 pip install

#scrapyd
scrapyd-deploy -p myspider

scrapyd-deploy -p suumo_rent.jp

pipreqs ./ --encoding=utf8 
``
备份:mongodump -h 127.0.0.1:12001 --collection log_aliyun_operation --db log --gzip --archive=/home/20180407.archive

还原:mongorestore  -h 127.0.0.1:12001--gzip --archive=/home/20180407.archive

curl http://localhost:6800/schedule.json -d project=Summo_2 -d spider=suumo_rent.jp

curl http://localhost:6800/listprojects.json （列出项目）
curl http://localhost:6800/listspiders.json?project=myspider （列出爬虫）
curl http://localhost:6800/listjobs.json?project=myspider （列出job）
curl http://localhost:6800/cancel.json -d project=myspider -d job=tencent （终止爬虫，该功能会有延时或不能终止爬虫的情况，此时可用kill -9杀进程的方式中止）


docker-compose up --build -d


mongodump --db ba_stock --out /mnt
mongodump --db ba_stock --out /mnt/back_up --collection summo