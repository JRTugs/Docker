# Docker run Commands

Create and run a new container from an image
```bash
docker run <image_name:tag>
```

## Docker run
```bash
docker run jodo0131/helloworld:latest
```

## Docker run in background
```bash
docker run -d jodo0131/helloworld:latest 
```

## Docker run in background with port mapping
docker run -p 8080:8080 [Image ID]
```bash
docker run -d -p 8080:8080 jodo0131/helloworld:latest
```

## Docker run in background with port mapping and assigning name for container
```bash
docker run -d -p 8080:8080 --name helloworld jodo0131/helloworld:latest
```
<img width="628" alt="image" src="https://github.com/user-attachments/assets/57d58805-793f-41ac-b743-d237f40fb415">

## Run container interactively and can run commands inside the containter
docker run -it [image] [command-or-shell]
```bash
docker run -it jodo0131/helloworld:latest /bin/bash
```
<img width="314" alt="image" src="https://github.com/user-attachments/assets/8b60bed9-68de-418a-accf-fd0b07bec5b5">

```bash
docker run -it jodo0131/helloworld:latest ls
```
<img width="276" alt="image" src="https://github.com/user-attachments/assets/6d7e5722-4dd4-4ae3-a172-9a0292c82b2b">

## Run Container and Mount Host Volumes
docker run -v [path-on-host]:[path-inside-container] [image]
```bash
docker run -v /root/docker/:/app/docker jodo0131/helloworld:latest
```

## Run Container and remove it once containter stops
docker run --rm [image]
```bash
docker run -d --name helloworld --rm jodo0131/helloworld:latest
```


















