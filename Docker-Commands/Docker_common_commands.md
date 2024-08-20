# Docker Common Commands

## Docker Version
```bash
docker version
```
## Docker Search for images in docker hub
Recommended to choose Offcial image from docker hub
```bash
docker search redis
```

## Docker pull
```bash
docker pull redis:latest
```

## List all running container and all exited
```bash
docker ps -a 
```

## Stop container
docker stop [CONTAINER ID]
```bash
docker stop 269ca7e4693d
```

## Restart container
docker restart [CONTAINER ID]
```bash
docker restart 269ca7e4693d
```

## Docker kill immediately killing container
docker kill [CONTAINER ID]
```bash
docker kill 269ca7e4693d
```






