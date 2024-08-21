# 1. Docker Commands

* ## Check docker version:

    ```bash
    docker version
    ```

    ```bash
    docker -v
    # OR
    docker --version
    ```

* ## Test Docker Installation:

    ```bash
    docker run hello-world
    ```

# 2. Docker Image Commands

* ## Building the Image for Dev:

    ```bash
    docker build -f Dockerfile.dev -t my-dev-image .
    ```

* ## Check Images:

    ```bash
    docker images
    ```

    ```bash
    docker image ls
    ```
* ## Verify the config:

    ```bash
    docker inspect my-dev-image
    ```

* ## Building fully optimized Image for Production:

    ```bash
    docker build -f Dockerfile.prod -t my-prod-image-optimized .
    ```

# 3. Docker Container Commands

* ## List Running Containers:

    ```bash
    docker ps
    ```

* ## List all Containers:

    ```bash
    docker ps -a
    
    # -a flag shows the list of all existing containers whether it is running or not
    ```
    
* ## Start the Existing Container

    ```bash
    docker start <container-name/ id/ id(4-digits)>
    ```

* ## Stop the Running Container

    ```bash
    docker stop <container-name/ id/ id(4-digits)>
    ```
    
* ## Delete the Container

    ```bash
    docker rm <container-name/ id/ id(4-digits)>

    # To delete or remove the container, make sure it is existed and stopped
    ```

* ##  Running the Container for Dev:

    ```bash
    docker run -d --name dev-cont1 -p 8000:8000 <image-id/name>
    
    # 8000:8000 [hosting port (changeable) : container port]
    ```

* ##  Running the Temporary Container for Dev:

    ```bash
    docker run -d --rm --name dev-cont1 -p 8000:8000 <image-id/name>
    
    # --rm flag removes the container when we stop thats why it is called the temporary container
    ```

* ## Running the Container for Production:

    ```bash
    docker run -d -p 8000:8000 my-prod-image-optimized
    ```

* ## container logs:

    ```bash
    docker logs dev-cont1
    ```

* ## Test the Container:

    ```bash
    docker run -it --rm my-dev-image /bin/bash -c "poetry run pytest"
    ```

* ## Intract with the Container:

    ```bash
    docker exec -it dev-cont1 /bin/bash
    ```

* ## Exit from the container shell:

    ```bash
    exit
    ```
