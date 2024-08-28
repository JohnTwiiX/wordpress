# wordpress

with Docker compose

## Introduction

This is a docker compose example of how to set up a wordpress with a mariadb.

### Install Docker Compose

1. download and install te Compose CLI

    ```bash
    DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
    mkdir -p $DOCKER_CONFIG/cli-plugins
    curl -SL https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
    ```

1. apply executable permissions to the binary

    ```bash
    chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
    ```

    or, if you chose to install Compose for all users:

    ```bash
    sudo chmod +x /usr/local/lib/docker/cli-plugins/docker-compose
    ```

1. test the installation

    ```bash
    docker compose version
    ```

### Run Docker Compose file

1. Configure the environment variables.
    1. Copy the content of the example env file that is inside the wordpress folder into a .env file:

        ```bash
        cp simple_env_config.env .env
        ```

    1. The new .env file should contain all the environment variables necessary to run all the app in all the environments. However, the only needed variables for the development environment to run are the following:

        ```bash
        DB_HOST=
        DB_USER=
        DB_PASSWORD=
        DB_NAME=
        MYSQL_ROOT_PASSWORD=
        ```

    1. For the database, the default configurations should be:

        ```bash
        DB_HOST=db
        DB_USER=wordpress
        DB_PASSWORD=wordpress
        DB_NAME=wordpress
        MYSQL_ROOT_PASSWORD=example_root_password
        ```

1. run docker compose

    ```bash
    docker compose up
    ```
