# Docker cheatsheet

## Build
```bash
docker build -t my-img .

docker build --no-cache --build-arg NODE_ENV=${NODE_ENV} -t my-img .

docker build -t my-img -f=my-dockerfile .
```

## Run
```bash
docker run -d -p 8082:8082 -v $(pwd)/data/logs:/data/logs -e 'NODE_ENV=dev' --name my-img my-img

docker run -it --name my-img my-img
```

## Exec
```bash
docker exec -it my_image sh
```

## Stop & Delete
```bash
docker ps -a

docker stop -t0 my-img

docker rm my-img
docker rm `docker ps -a -q`
```

## Remove images
```bash
docker images

docker rmi --force $(docker images -q)
or
docker images -q |xargs docker rmi

# remove all unused images
docker rmi $(docker images --filter "dangling=true" -q --no-trunc)
```

## Remove all volumes
```bash
docker volume rm $(docker volume ls -q --filter dangling=true)
```



## Run a Python 3 Debian image locally
```bash
docker run -it --name python python:3.7.3-slim sh
```

## Run a Node 14 image locally, and mount the current folder
```bash
docker run -it -v ~/mypath:/app --name node14 node:14.17.5-bullseye-slim sh
```

## Launch a MongoDB instance locally
```bash
docker run --name mongo -p 127.0.0.1:27017:27017 -d mongo
```

## Launch a MySQL instance locally
```bash
docker run --name mysql -e MYSQL_ROOT_PASSWORD=yolo -e MYSQL_DATABASE=mydb -p 127.0.0.1:3306:3306 -d mysql:5.6.39
mysql -pyolo -uroot -h 127.0.0.1 -P 3306 mydb
```

## Launch an ElasticSearch instance locally
```bash
docker run --name elasticsearch -p 127.0.0.1:9200:9200 -d elasticsearch
docker run --name kibana -e ELASTICSEARCH_URL=http://127.0.0.1:9200 -p 5601:5601 -d kibana:latest
```


## Clean up
```bash
docker system prune -f
```

## Usefull links
  * [[http://blog.arungupta.me/docker-common-commands-cheatsheet-techtip59/|Docker Common Commands Cheatsheet (Tech Tip #59)]]
  * [[https://docker-curriculum.com/|A Docker tutorial for beginners]]
