# wordpress

with Docker compose

## Introduction

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

1. run docker compose

    ```bash
    docker compose up
    ```
