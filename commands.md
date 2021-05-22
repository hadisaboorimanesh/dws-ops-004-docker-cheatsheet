  
docker  pull nginx:1.20.0
docker image inspect nginx:1.20.0 | jq .[0].Config.ExposedPorts
docker inspect  nginx:1.20.0 |jq .[0].DockerVersion
---------------------------------------------------------
docker save nginx:1.20.0 -o  nginx.tar.gz
docker  rmi  nginx:1.20.0
 docker load -i nginx.tar.gz
--------------------------------------------------------------
 docker run -d -it --name nginx -p 8081:80  nginx:1.20.0
---------------------------------
 docker image prune
