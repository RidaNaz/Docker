# Docker Image Commands

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