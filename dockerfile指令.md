## docker build
```
docker build -t 名稱 .
```
## docker run
```
docker run 名稱
docker run image_id
```
## Docker 移除停用指令
```
https://medium.com/@william._./docker-%E7%A7%BB%E9%99%A4%E5%81%9C%E7%94%A8%E6%8C%87%E4%BB%A4-%E4%B8%89-e71c06f56b30
```
### 查看現有 Docker Image
```
docker images
docker image ls
```
### 刪除 Docker Image
```
docker rmi image_id
docker rmi 名稱
強制刪除:docker rmi -f image_id
```
### 查看現有 Container
```
docker ps -a
```
### 停用及刪除 Container
```
docker stop container_id
docker rm container_id
```
### 停用及刪除所有 Container 
```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```
