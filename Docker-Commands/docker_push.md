# Docker Push Commands

Upload an image to a registry

Syntax:
docker image push [OPTIONS] NAME[:TAG]

## Push image to registry
```bash
docker push jodo0131/helloworld:latest
```

## Push all image to registry
```bash
docker push -a 
```

## Push image with all tags
Will upload all images with repository name "jodo0131/helloworld"
```bash
docker image push --all-tags jodo0131/helloworld
```
<img width="292" alt="image" src="https://github.com/user-attachments/assets/fbe096ef-fde6-4281-9c03-470c0a8aa5b8">




