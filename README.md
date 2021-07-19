# node-docker-redis

We will create `Dockerfile` and `docker-compose.yml` files purely hands-on from sratch to run Node API and cache the content with Redis.

## Usage
_note: first time it will load data from server and second or more times will be loaded from cache until its expired._


- http://localhost:8080/api/v1/users/Bret
- [Get list of Usernames](https://jsonplaceholder.typicode.com/users)

```sh
docker ps -a # list of all running/stopped/exited containers
docker images -a # list of images
docker volume ls # list of volumes
docker network ls # list of networks
docker network inspect bridge # inepect about bridge network

docker-compose up -d # start container at background
docker-compose down -v # shutdown/remove container with volumes

# check logs to see error, if containers don't work
docker logs redis
docker logs api

docker rmi -f $(docker images -aq) # remove all images if linked to stopped/removed containers
docker system prune -a --volumes # cleanup/remove everything (images, containers, volumes & etc) in one go
```

## Useful links
- [Dockerfile reference](https://docs.docker.com/engine/reference/builder/#from)
- [docker-compose v3 reference](https://docs.docker.com/compose/compose-file/compose-file-v3/)
- [node image](https://hub.docker.com/_/node?tab=tags)
- [redis image](https://hub.docker.com/_/redis?tab=tags)
