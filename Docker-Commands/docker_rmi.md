# Docker Images Remove Commands

Remove one or more images

Syntax: 

docker image rm [IMAGE]

docker rmi [IMAGE]

## Docker remove
```bash
docker rmi fd484f19954f
```

## Docker remove all images iwth same image ID
```bash
docker rmi -f fd484f19954f
```

## Docker remove using digests
Show digest for each images

```bash
docker images --digests
```

<img width="631" alt="image" src="https://github.com/user-attachments/assets/cc70cff4-2b5a-41b2-85db-34be5de43764">


Then run

```bash
docker rmi hello-world:latest@sha256:53cc4d415d839c98be39331c948609b659ed725170ad2ca8eb36951288f81b75
```


