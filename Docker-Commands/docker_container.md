# Docker Container Commands

| Commands  | Description |
| ------------- | ------------- |
| **docker container attach**  | Attach local standard input, output, and error streams to a running container |
| **docker container commit**  | Create a new image from a container's changes |
| **docker container cp**  | Copy files/folders between a container and the local filesystem |
| **docker container create**  | Create a new container |
| **docker container diff**  | Inspect changes to files or directories on a container's filesystem |
| **docker container export**  | Export a container's filesystem as a tar archive |
| **docker container inspect**  | Display detailed information on one or more containers |
| **docker container kill**  | Kill one or more running containers |
| **docker container logs**  | Fetch the logs of a container |
| **docker container pause**  | Pause all processes within one or more containers |
| **docker container port**  | List port mappings or a specific mapping for the container |
| **docker container prune**  | Remove all stopped containers |
| **docker container rename**  | Rename a container |
| **docker container restart**  | Restart one or more containers |
| **docker container rm**  | Remove one or more containers |
| **docker container start**  | Start one or more stopped containers |
| **docker container stats**  | Display a live stream of container(s) resource usage statistics |
| **docker container stop**  | Stop one or more running containers |
| **docker container top**  | Display the running processes of a container |
| **docker container unpause**  | Unpause all processes within one or more containers |
| **docker container update**  | Update configuration of one or more containers |
| **docker container wait**  | Block until one or more containers stop, then print their exit codes |
| **docker container exec**  | Execute a command in a running container |
| **docker container ls**  | List containers |
| **docker container run**  | Create and run a new container from an image |


## Docker Copy
Copy files from local into container
```bash
docker cp sample.txt helloworld:/app
```

Copy files from container into local file system
```bash
docker cp helloworld:/app/sample.txt /tmp/
```

## Docker Create
Creates new container from an image without starting it

```bash
docker container create --name redis redis:latest
```

## Docker Diff
```bash
docker container diff redis
```

## Docker Container Export
```bash
docker export redis > redis.tar
```
## Docker Port
```bash
docker port redis
```

## Docker Container prune
```bash
docker container prune -f
```

## Docker Container Rename
```bash
docker container rename redis redis2
```

## Docker Container Stats
```bash
docker stats
```

## Docker Top
```bash
docker container top redis
```

## Docker Pause
```bash
docker container pause redis
```

## Docker Unpause
```bash
docker container unpause redis
```

## Docker Update
```bash
docker update --kernel-memory 80M redis
```






