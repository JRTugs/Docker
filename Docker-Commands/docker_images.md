# Docker Images Command

| Commands  | Description |
| ------------- | ------------- |
| **docker image history**  | Show the history of an image |
| **docker image import**  | Import the contents from a tarball to create a filesystem image |
| **docker image inspect**  | Display detailed information on one or more images |
| **docker image load**  | Load an image from a tar archive or STDIN |
| **docker image prune**  | Remove unused images |
| **docker image rm**  | Remove one or more images |
| **docker image save**  | Save one or more images to a tar archive (streamed to STDOUT by default) |
| **docker image tag**  | Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE |
| **docker image ls**  | List images |
| **docker image pull**  | Download an image from a registry |
| **docker image push**  | Upload an image to a registry |

## Docker Load
```bash
docker load < busybox.tar.gz
```

## Docker Save
```bash
docker save busybox > busybox.tar
```

```bash
docker save -o fedora-latest.tar fedora:latest
```

## Docker Tag
```bash
ocker tag redis redis/redis:version1.0
```

