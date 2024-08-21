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

    # It pulls the image of hello-world from the Docker Hub and run container on this image
    ```

# 2. Docker Image Commands

* ## Check Images:

    ```bash
    docker images
    ```

    ```bash
    docker image ls
    ```

* ## Delete Image:

    ```bash
    docker rmi <image-name/ id/ id(4-digits)>

    # To delete the image, make sure you have stopped and delete all the containers that are run on that image
    ```

    ```bash
    docker rmi <image-name>:<version>

    # To delete a specific version of the image
    ```

* ## Building the Image for Dev:

    ```bash
    docker build -f Dockerfile.dev -t my-dev-image .

    # -t flag is used to give name of the image
    ```

    ```bash
    docker build -t <image-name>:v1 .

    # v1 is used to give the version of the image which shows in Tag
    ```

* ## Building fully optimized Image for Production:

    ```bash
    docker build -f Dockerfile.prod -t my-prod-image-optimized .
    ```

* ## Verify the config:

    ```bash
    docker inspect <image-name/id>
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
    
* ## Start the Existing Container:

    ```bash
    docker start <container-name/ id/ id(4-digits)>
    ```

* ## Stop the Running Container:

    ```bash
    docker stop <container-name/ id/ id(4-digits)>
    ```
    
* ## Delete the Container:

    ```bash
    docker rm <container-name/ id/ id(4-digits)>

    # To delete or remove the container, make sure it is existed and stopped
    ```

* ##  Running the Container for Dev:

    ```bash
    docker run -d --name dev-cont1 -p 8000:8000 <image-id/name>
    
    # -d flag refers to the de-attach mode, means container run in the background
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

* ## Test the Container:

    ```bash
    docker run -it --rm my-dev-image /bin/bash -c "poetry run pytest"
    ```

* ## Intract with the Container:

* while interacting with the container make sure that the container is running.

    ```bash
    docker exec -it <container-id> /bin/bash

    # -it flag is used to interact with the container
    # /bin/bash shows the folder name in which you are in container
    ```

    ```bash
    docker exec -it <container-id> sh

    # sh works like /bin/bash but does not show the directory name
    ```

* ## Exit from the container shell:

    ```bash
    exit

    # After interacting with the container, you are in the container shell, to exit from it, run this command
    ```

* ## Container Logs:

    ```bash
    docker logs <container-id/name>
    ```

* ## Inspect Container:

    ```bash
    docker inspect <container-id/name>
    ```

* ## Container Statistics:

    ```bash
    docker stats <container-id/name>
    ```

# 4. Docker Volume Commands

* ## Volume Documentation:

    ```bash
    docker volume --help
    ```

* ## List of all Volumes:

    ```bash
    docker volume ls
    ```

* ## Inspect Volume:

    ```bash
    docker volume inspect <volume-name>
    ```

* ## Create Volume:

    ```bash
    docker volume create <volume-name>
    ```

    ```bash
    docker volume create --driver local \

    # If you does not provide volume name, it gives random name to that volume
    # By default the driver path is local, You also give you cloud path instead of local
    ```

* ## Use Volume in Container:

- You can use the volume in a container after creating it.
- When you delete container (that uses volume), only the container deletes not the volume.
- Because the volume is of outside the container.

    ```bash
    docker run -d -v <volume-name>:</folder-name> --name <container-name> <image-name>

    # -v flag refers to the existed volume to use in container
    # :</folder-name> makes folder inside the volume
    ```

* ## Delete Volume:

    ```bash
    docker volume rm <volume-name>
    ```