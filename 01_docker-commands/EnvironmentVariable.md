# Environment Variable Commands

* ## Declare Environment Variable while Running Container

    ```bash
    docker run -d -e KEY=value --name <container-name> <image-name>

    # -e flag refers to the environment variable to be declare
    ```

    ```bash
    docker run -d -e KEY=value -e KEY=value --name <container-name> <image-name>

    # If you have more than one variable, you can simply declare again with -e flag
    ```

* ## Refer the Environment Variable File:

    ```bash
    docker run -d --env-file <.env filename> --name <container-name> <image-name>

    # --env-file flag refers to the file where the environment variavbles are existed
    ```