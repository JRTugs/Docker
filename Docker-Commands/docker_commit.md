# Docker Commit Commands

The Docker Commit image is used to create a NEW IMAGE from the changes made to the Docker container. 
Docker commit can save the current state of the container in the form of a Docker image.

Syntax:
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
 docker commit <container_id> <new_image_name>

## Commit using defaults
```bash
docker commit b9f7c1bf82ff new_helloworld
```

## Commit with Author Information
```bash
docker commit -a "Author Name" b9f7c1bf82ff new_helloworld
```
Author name can be found in docker inspect image_id

## Commit with a commit message
```bash
 docker commit -m "Added new features"  b9f7c1bf82ff new_helloworld
```
Comments can be found in docker inspect image_id

## Commit with changes Applied
```bash
docker commit --change="ENV DEBUG=true" b9f7c1bf82ff new_helloworld
```
Changes in ENV can be found in docker inspect image_id





