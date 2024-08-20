# Docker exec Commands

Execute a command in a running container

Syntax:
docker exec <container-id-or-name> <command>


## Run command in container
```bash
docker exec 5013b48d1463 ls /app
```

## Run an Interactive Bash Shell
```bash
docker exec -it 5013b48d1463 /bin/bash
```

## Run command as different username
```bash
docker exec -u user 5013b48d1463 whoami
```

## Running Commands in an Alternate Directory in a Docker Container
```bash
docker exec --workdir /opt 5013b48d1463 pwd
```

## Running Commands as a Different User in a Docker Container
```bash
docker exec --user user1 5013b48d1463 yum update
```

## Running two commands
```bash
docker exec 5013b48d1463 sh -c "date;cal"
```


