# Docker Network Commands

* ## Network Documentation:

    ```bash
    docker network --help
    ```
    
* ## List of Networks:

    ```bash
    docker network ls
    ```

* ## Create Network:

    ```bash
    docker network create <network-name>
    ```

* ## Connect Network to Container:

- You can connect the network to a container after creating it.
- When you delete container (that connects network), only the container deletes not the network.
- Because the network is created outside of the container.

    ```bash
    docker connect <network-name> <container-name>
    ```
    
* ## Disconnect Network from Container:

    ```bash
    docker disconnect <network-name> <container-name>
    ```

* ## Connect Network and Run Container:

- You can connect the network to a container after creating it.
- When you delete container (that connects network), only the container deletes not the network.
- Because the network is created outside of the container.

    ```bash
    docker run -d --network=<network-name> --name <container-name> <image-name>
    ```

* ## Inspect Network:

    ```bash
    docker network inspect <network-name>
    ```

* ## Delete Network:

    ```bash
    docker network rm <network-name>
    ```