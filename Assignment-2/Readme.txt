Steps after creating the Dockerfile. Run the following commands via terminal in the same directory as the docker file:
1 docker build -f Dockerfile -t go-app ..
2 docker run -d --name go-app-1 -p 8080:8080 go-app
    curl http://localhost:8080/
3 docker tag go-app:latest nitin6548/go-app:v1
4 docker history nitin6548/go-app:v1
5 docker login
6 docker push nitin6548/go-app:v1
