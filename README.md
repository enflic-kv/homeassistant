# Homeassistant & CodeServer powered by docker compose

## Requirements

* docker >= 17.12.0+
* docker-compose

## Quick Start

1. Install [docker-compose](https://docs.docker.com/compose/install/) on the docker host.
2. Clone this repo on the docker host.
3. Navigate to the directory,  `cd homeassistant`
4. Use configuration and update the variables in .env file.

   ```bash
   mv .env-template .env
   nano .env
   ```

5. Run the following command from the root:

    ```bash
    docker-compose up -d
    ```

6. To stop the app, run the following command from the root of the cloned repo:

    ```bash
    docker-compose down
    ```

7. Create a long-lived-token from HA and include the token in .env file under **HA_TOKEN** variable.

## Environments

This Compose file contains the following environment variables:

| Variables | Default value |
| --------- | -------- |
| HA_IMAGE_VERSION | latest |
| HA_CONTAINER_NAME | home-assistant-container |
| HA_URL | <http://localhost:8123> |
| HA_TOKEN | **required** |
| HA_MEDIA_PATH | ./media |
| CODE_SERVER_IMAGE_VERSION | latest |
| CODE_SERVER_CONTAINER_NAME | vscode-server-container |
| CODE_SERVER_PUID | 1000 |
| CODE_SERVER_PGID | 1000 |
| CODE_SERVER_TZ | Asia/Kuala_Lumpur |
| CODE_SERVER_PASSWORD | administrator |
| EXTERNAL_NETWORK | homelab-local |
