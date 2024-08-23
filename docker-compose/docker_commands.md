# commands

# create docker network
docker network create mongo-network

## start mongodb
docker run -d \
-p 27017:27017 \
-e MONGO_INITDB_ROOT_USERNAME=admin \
-e MONGO_INITDB_ROOT_PASSWORD=password \
--net mongo-network \
--name mongodb \
mongo

## start mongo-express
docker run -d \
-p 8081:8081 \
-e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
-e ME_CONFIG_MONGODB_ADMINPASSWORD=password \
-e ME_CONFIG_MONGODB_SERVER=mongdob \
--net mongo-network \
--name mongo-express \
mongo-express

## docker up
Start all container in docker-compose
```bash
docker-compose -f mongo-services.yaml up -d
```

## docker down
Shutdown all container in docker-compose
```bash
docker-compose -f mongo-services.yaml down
```

Note: UP and DOWN command will shutdown the container and removing any data in the databases running inside the container.

## Docker start
```bash
docker-compose -f mongo-services.yaml down -d
```

## Docker Stop
Container are just in exited status
```bash
docker-compose -f mongo-services.yaml stop
```
Note: STOP command will just exit the container thus retaining any data in the databases running inside the container.

