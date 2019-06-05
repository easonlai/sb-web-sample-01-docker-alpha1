# Sample Java Web App in Spring Boot framework with Containerization (variant to show TCP port change)
Readme update 1.0

## Build with Maven
```shell
mvn package
```

## Run locally
```shell
java -jar target/gs-spring-boot-docker-0.1.0.jar -server.port=80
```

## Test web app locally
```shell
http://localhost
```

## Containerize
1. Build a docker image using `Dockerfile`:
   ```
   docker build -t sb-web-sample-01-docker-alpha1 .
   ```
2. Run docker image locally
   ```
   docker run --rm -p 80:80 sb-web-sample-01-docker
   ```
3. Then you can access the web app at http://localhost in browser.

Or you can pull this sample from my Docker Hub.
https://cloud.docker.com/u/easonlai/repository/docker/easonlai/sb-web-sample-01-docker-alpha1

## Deploy to K8S
```shell
kubectl apply -f sb-web-sample-01-docker-kube.yaml
```
