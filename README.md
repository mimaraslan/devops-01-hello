# DevOps 

### Docker Documentation


```
docker login -u           mimaraslan    -p          123456789

docker login --username   mimaraslan    --password  123456789

docker login -u           mimaraslan    --password  123456789

```

```
docker run    --name   my-postgres   -e POSTGRES_USER=postgres    -e POSTGRES_PASSWORD=123456789   -e POSTGRES_DB=postgres  -p 9999:5432    -d postgres
```


### ===============  kendi jarlarımızı image olarak docker'a verme  ====================== 

```
docker build    --build-arg   JAR_FILE=target/devops-01-hello-1.0.1.jar      --tag mimaraslan/devops-01-hello:v001   .
```

```
docker build    --build-arg   JAR_FILE=target/devops-01-hello-1.0.1.jar      --tag mimaraslan/devops-01-hello:latest   .
```


```
docker build    --build-arg   JAR_FILE=target/devops-01-hello-1.0.2.jar      --tag mimaraslan/devops-01-hello:v002   .
```

```
docker build    --build-arg   JAR_FILE=target/devops-01-hello-1.0.2.jar      --tag mimaraslan/devops-01-hello:latest   .
```


```
docker build    --build-arg   JAR_FILE=target/devops-01-hello-1.0.3.jar      --tag mimaraslan/devops-01-hello:v003   .
```

```
docker build    --build-arg   JAR_FILE=target/devops-01-hello-1.0.3.jar      --tag mimaraslan/devops-01-hello:latest   .
```



### ===============  kendi imagelerimizi container olarak çalıştırma ====================== 


```
docker           run       -it     -d           --name my-app1         -p 8081:8080                      mimaraslan/devops-01-hello:v001
```

```
docker container run       -it     -d           --name my-app1         -p 8081:8080                      mimaraslan/devops-01-hello:v001
```

```
docker  run       -it     -d           --name my-app2         -p 8082:8080                      mimaraslan/devops-01-hello:v002
```

```
docker  run       -it     -d           --name my-app3         -p 8083:8080                      mimaraslan/devops-01-hello:latest
```

```
docker  run       -it     -d           --name my-app4         -p 8084:8080                      mimaraslan/devops-01-hello
```



===============  kendi imagelerimizi dockerhub'a gönderme  ======================

docker push mimaraslan/devops-01-hello:v001
docker push mimaraslan/devops-01-hello:v002
docker push mimaraslan/devops-01-hello:latest
docker push mimaraslan/devops-01-hello


===============  kendi imagelerimizi dockerhub'dan çekme  ======================

docker pull mimaraslan/devops-01-hello:v001
docker pull mimaraslan/devops-01-hello:v002
docker pull mimaraslan/devops-01-hello:latest
docker pull mimaraslan/devops-01-hello


