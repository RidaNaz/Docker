# Docker Compose

- **Simplify Multi-Container Applications:** Manage and run multiple containers with a single command.

- **Automate Setup:** Automatically configure and link containers according to the defined services.

- **Ensure Consistency:** Maintain consistent environments across development, testing, and production.

- **Easily Scale Services:** Scale containers up or down as needed with minimal effort.

- **Centralize Configuration:** Keep all container configurations in a single, easy-to-manage docker `compose.yml` file.

# Docker Compose Commands

* ## Docker Compose Version:

    ```bash
    docker-compose -v
    ```

* ## Run and Start the Container (mentioned in .yaml file)

    ```bash
    docker compose up -d
    ```

* ## Stop Running Container

- It only stops the container, not remove.

    ```bash
    docker compose stop
    ```

* ## Restart the previously Stopped Container

    ```bash
    docker compose start
    ```

* ## Stop and Delete the Container

- Stops and removes all the containers, networks, and volumes created by `docker compose up`.

    ```bash
    docker compose down
    ```