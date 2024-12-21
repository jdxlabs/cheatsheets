# Podman cheatsheet

## Install
```bash
apt install podman podman-compose
```

## Build
```bash
podman build -t my-img .

podman build --no-cache --build-arg NODE_ENV=${NODE_ENV} -t my-img .

podman build -t my-img -f=my-podmanfile .
```

## Run
```bash
podman run --rm -d -p 8080:80 --name web docker.io/library/nginx

watch podman ps
podman stop -t0 web
podman images
podman rmi docker.io/library/nginx

# other examples
podman run -d -p 8082:8082 -v $(pwd)/data/logs:/data/logs -e 'NODE_ENV=dev' --name my-img my-img
podman run -it --name my-img my-img
```

## Exec
```bash
podman exec -it my_image sh
```

## Stop & Delete
```bash
podman ps -a

podman stop -t0 my-img

podman rm my-img
podman rm `podman ps -a -q`
```

## Remove images
```bash
podman images

podman rmi --force $(podman images -q)
or
podman images -q |xargs podman rmi
```

## Remove all unused images
```bash
podman rmi $(podman images --filter "dangling=true" -q --no-trunc)
```

## Remove all volumes
```bash
podman volume rm $(podman volume ls -q --filter dangling=true)
```

## Run a Python 3 Debian image locally
```bash
podman run -it --name python docker.io/library/python:3.7.3-slim sh
```

## Run a Node 14 image locally, and mount the current folder
```bash
podman run -it -v ~/mypath:/app --name node14 docker.io/library/node:14.17.5-bullseye-slim sh
```

## Launch a MongoDB instance locally
```bash
podman run --name mongo -p 127.0.0.1:27017:27017 -d docker.io/library/mongo
```

## Launch a MySQL instance locally
```bash
podman run --name mysql -e MYSQL_ROOT_PASSWORD=yolo -e MYSQL_DATABASE=mydb -p 127.0.0.1:3306:3306 -d docker.io/library/mysql:5.6.39
mysql -pyolo -uroot -h 127.0.0.1 -P 3306 mydb
```

## Launch an ElasticSearch instance locally
```bash
podman run --name elasticsearch -p 127.0.0.1:9200:9200 -d docker.io/library/elasticsearch
podman run --name kibana -e ELASTICSEARCH_URL=http://127.0.0.1:9200 -p 5601:5601 -d docker.io/library/kibana:latest
```

## Clean up
```bash
podman system prune -f
```

## Usefull links
* [Podman Documentation](https://docs.docker.io/en/latest/)
* [Podman CLI cheatsheet](https://mpolinowski.github.io/docs/DevOps/Linux/2019-09-25--podman-cheat-sheet/2019-09-25/)
