Steps to attach a volume to an nginx container and make changes in the volume folder. Mount another container with the same volume and compare changes. Run the following commands to do so:
1 docker volume create  my_volume
2 docker run -d -v my_volume:/usr/share/nginx/html --name nginx-container-1 -p 8080:80 nginx
3 docker exec -it nginx-container-1 /bin/bash
    cd /usr/share/nginx/html
    echo "Hello World" > index.html
    exit
5 curl http://localhost:8080 #gives output as Hello World
4 docker run -d -v my_volume:/usr/share/nginx/html --name nginx-container-2 -p 8081:80 nginx
6 curl http://localhost:8081 #gives output as Hello World
