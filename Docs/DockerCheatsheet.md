## Dockerfile
### Building specific container
```
docker build -t container-name
```

### Running specific container
```
# Run in background and maps host port to container port
docker run -dp 127.0.0.1:3000:3000 container-name

# Run and open terminal
docker run -i -t container-name /bin/bash
```

### Execute terminal in contatiner
```
docker exec -it container-name /bin/bash
```

## List, stop and remove container
```
docker ps

docker stop <the-container-id>
docker rm <the-container-id>

# stop and remove shorthand
docker rm -f <the-container-id>
```


sudo docker-compose up --build -d


## Passing Arguements
### To docker-compose.yml
1. Create a external .env file
