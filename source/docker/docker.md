
## Docker 
Docker 提供了虚拟化，隔离的系统环境

save an image
```
docker save -o imgname.tar imgname:version
gzip imgname.tar
```

access in iteractive mode
```
docker exec -it container-name bash
```

remove all exited containers
```
docker rm $(docker ps -a -f status=exited -q)
```
