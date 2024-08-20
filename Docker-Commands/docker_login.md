# Docker Login Commands

Log in to a registry
When you log in, the command stores credentials in $HOME/.docker/config.json

## Interactively log into a registry
```bash
docker login
```

## Log into a registry with a specific username (user will be prompted for a password):
```bash
docker login --username user1
```

## Log into a registry with username and password:
```bash
docker login --username user1 --password password server
```

## Log into a registry with password from stdin
```bash
echo "password" | docker login --username user1 --password-stdin
```

```bash
cat ~/my_password.txt | docker login --username user1 --password-stdin
```

