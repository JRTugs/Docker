# Docker remove Commands

Remove one or more containers 

**Syntax:**

docker container rm [OPTIONS] CONTAINER [CONTAINER...]

docker rm [OPTIONS] CONTAINER [CONTAINER...]


## Remove a container
```bash
docker rm helloworld
```
## Forcefully remove a container
```bash
docker rm -f jodo0131/helloworld:latest
```
The main process inside the container referenced under the link redis will receive SIGKILL, then the container will be removed.

## Removed all stopped containers
Using filter
```bash
docker rm $(docker ps --filter status=exited -q)
```
Using xargs
```bash
docker ps --filter status=exited -q | xargs docker rm
```

## Remove a container and its volumes
```bash
docker rm --volumes helloworld
```

## Remove a container and selectively remove volumes
```bash
docker create -v awesome:/foo -v /bar --name hello redis
hello

docker rm -v hello
```



