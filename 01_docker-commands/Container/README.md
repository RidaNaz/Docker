# Docker Container Commands

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

    ```bash
    docker rm <container-name/ id/ id(4-digits)> -f

    # -f flag removes the container forcefully, so there is no need to stop the container before removing
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
    docker container inspect <container-id/name>
    ```

* ## Container Statistics:

    ```bash
    docker stats <container-id/name>
    ```