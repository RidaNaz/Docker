# Docker Volume Commands

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

* ## Use Volume and Run Container:

- You can use the volume in a container after creating it.
- When you delete container (that uses volume), only the container deletes not the volume.
- Because the volume is created outside of the container.

    ```bash
    docker run -d -v <volume-name>:</folder-name> --name <container-name> <image-name>

    # -v flag refers to the existed volume to use in container
    # :</folder-name> makes folder inside the volume
    ```

* ## Delete Volume:

    ```bash
    docker volume rm <volume-name>
    ```
