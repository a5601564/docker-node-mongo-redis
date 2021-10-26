docker-compose -f docker-compose-dev.yml up


docker-compose -f docker-mongodb.yml up

ports:
 
- "80:80" # 绑定容器的80端口到主机的80端口
 
- "9000:8080" # 绑定容器的8080端口到主机的9000端口
 
- "443" # 绑定容器的443端口到主机的任意端口，容器启动时随机分配绑定的主机端口号