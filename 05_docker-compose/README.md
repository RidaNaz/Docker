# Docker Compose

- Manage and run multiple containers with a single command.
- Automatically configure and link containers according to the defined services.
- Maintain consistent environments across development, testing, and production.
- Scale containers up or down as needed with minimal effort.
- Keep all container configurations in a single, easy-to-manage docker `compose.yml` file.
- Must visit [`compose.yaml`](/05_docker-compose/compose.yaml) file!

# Docker Compose Commands

* ## Docker Compose Version:

    ```bash
    docker-compose -v
    ```

* ## Run and Start the Container (mentioned in .yaml file)

    ```bash
    docker compose up -d
    # -d : runs container in de-attach mode
    ```

* ## Stop Running Container

   It only stops the container, not remove.

    ```bash
    docker compose stop
    ```

* ## Restart the previously Stopped Container

    ```bash
    docker compose start
    ```

* ## Stop and Delete the Container

   Stops and removes all the containers, networks, and volumes created by `docker compose up`.

    ```bash
    docker compose down
    ```

* ## Check Config of `compose.yaml`

  - Ensures your `compose.yaml` is syntactically *correct* and *valid*.
  - Helps identify issues in your configuration before you attempt to bring up the services.
  - Outputs a fully expanded configuration, showing all default values and resolving variable interpolations.

  ```bash
  docker compose config
  ```