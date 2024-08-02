# Some Docker Commands

### Check docker version:

```bash
docker version
```

```bash
docker -v
# OR
docker --version
```

### Test Docker Installation:

```bash
docker run hello-world
```

### Building the Image for Dev:

```bash
docker build -f Dockerfile.dev -t my-dev-image .
```

### Check Images:

```bash
docker images
```
### Verify the config:

```bash
docker inspect my-dev-image
```

###  Running the Container for Dev:

```bash
docker run -d --name dev-cont1 -p 8000:8000 my-dev-image
```

### container logs:

```bash
docker logs dev-cont1
```

### Test the Container:

```bash
docker run -it --rm my-dev-image /bin/bash -c "poetry run pytest"
```

### List Running Containers:

```bash
docker ps
```

### List all Containers:

```bash
docker ps -a
```

### Intract with the Container:

```bash
docker exec -it dev-cont1 /bin/bash
```

### Exit from the container shell:

```bash
exit
```

### Building fully optimized Image for Production:

```bash
docker build -f Dockerfile.prod -t my-prod-image-optimized .
```

### Running the Container for Production:

```bash
docker run -d -p 8000:8000 my-prod-image-optimized
```