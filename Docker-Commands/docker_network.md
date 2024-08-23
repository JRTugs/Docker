# Docker Network Commands

| Commands  | Description |
| ------------- | ------------- |
| **docker network connect**  | Connect a container to a network  |
| **docker network create**  | create	Create a network  |
| **docker network disconnect**  |	Disconnect a container from a network  |
| **docker network inspect**  |	Display detailed information on one or more networks  |
| **docker network ls**  |	List networks  |
| **docker network prune**  |	Remove all unused networks  |
| **docker network rm**  |	Remove one or more networks  |

## Docker network connect
Reference: https://docs.docker.com/reference/cli/docker/network/connect/

## Docker network create
Reference: https://docs.docker.com/reference/cli/docker/network/create/

## Docker network disconnect
Reference: https://docs.docker.com/reference/cli/docker/network/disconnect/

## Docker network inspect
Reference: https://docs.docker.com/reference/cli/docker/network/inspect/

## Docker network ls
Reference: https://docs.docker.com/reference/cli/docker/network/ls/

## Docker network prune
Reference: https://docs.docker.com/reference/cli/docker/network/prune/

## Docker network rm
Reference: https://docs.docker.com/reference/cli/docker/network/rm/

# BRIDGE
Creating bridge network is used when need to create own CIDR Block

## Create network
Create Bridge network
```bash
docker network create my-bridge-net --subnet 10.0.0.0/19 --gateway 10.0.0.1
```

Running an images with specific network
```bash
docker run -d --name helloworld -p 8080:8080 --network my-bridge-net jodo0131/helloworld
```

# HOST
Creating host network will used the Host IP thus not creating a CIDR Block. All containers using HOST network will have the same IP address as of the Host. Different Host server will be able to access the container port directly as if the application is running in the HOST and not in the container.

```bash
docker run -d --name helloworld --network host jodo0131/helloworld:latest
```

# None
Isolates container from Host and other containers. Only loopback interface will be created. Can be used to data processing pipelines
```bash
docker run -d --name helloworld --network none jodo0131/helloworld:latest
```

# IPvlan
IPVlan network creates a network with the same CIDR Block of the Host.

Create IPVlan network
```bash
docker network create -d ipvlan \
    --subnet=192.168.100.0/24 \
    --gateway=192.168.100.1 \
    -o ipvlan_mode=l2 \
    -o parent=enp0s3 my-ipvlan-net
```

```bash
docker run -d --name helloworld --network my-ipvlan jodo0131/helloworld:latest
```

Note: Container IP will now be different this time when connected to IPVlan as each container is now assigned different IP.

Host IP: 192.168.100.42
Container IP: 192.168.100.2
![image](https://github.com/user-attachments/assets/18bfe5e5-ccfa-43e4-8149-5731c83085ba)










