# ash-shell

> `ash` shell initialization for Node.js development
  in an Alpine Linux Docker container.

## Usage

Create an external shell volume for reuse.

### `docker-compose.yml`

    version: "3.6"
    services:
      app:
        environment:
          - ENV=/home/node/shell/ash.sh
          - PROJECT=PS1_TOKEN
        volumes:
          - shell:/home/node/shell
    volumes:
      shell:
        external: true
