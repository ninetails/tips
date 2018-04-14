# Programming/Docker

## Stop/Kill/Remove containers & Remove all images

```sh
# stop all containers:
docker stop $(docker ps -q)

# kill all containers:
docker kill $(docker ps -q)

# remove all containers
docker rm $(docker ps -a -q)

# remove all docker images
docker rmi $(docker images -q)
```

[Source](https://gist.github.com/weblancaster/6e7f43fc02725ce747e224b0c4290906)
