# docker-baseimage-alpine
A custom base image built with Alpine linux and S6 overlay.


## Usage

Here are some example snippets to help you get started creating a container.

### docker-compose (recommended, [click here for more info](https://docs.linuxserver.io/general/docker-compose))

```yaml
---
version: "2.1"
services:
  nginx:
    image: ghcr.io/alfinternet/baseimage-alpine
    container_name: baseimage-alpine
    restart: unless-stopped
```

### docker cli ([click here for more info](https://docs.docker.com/engine/reference/commandline/cli/))

```bash
docker run -d \
  --name=baseimage-alpine \
  --restart unless-stopped \
ghcr.io/alfinternet/baseimage-alpine
```

## Parameters

Container images are configured using parameters passed at runtime (such as those above). These parameters are separated by a colon and indicate `<external>:<internal>` respectively. For example, `-p 8080:80` would expose port `80` from inside the container to be accessible from the host's IP on port `8080` outside the container.

| Parameter | Function |
| :----: | --- |


## Building locally

If you want to make local modifications to these images for development purposes or just to customize the logic:

```bash
git clone https://github.com/ALFinternet/docker-baseimage-alpine.git
cd docker-baseimage-alpine
docker build \
  --no-cache \
  --pull \
  -t ghcr.io/alfinternet/baseimage-alpine:3.15 -t ghcr.io/alfinternet/baseimage-alpine:latest .

  docker push ghcr.io/alfinternet/baseimage-alpine:3.15
  docker push ghcr.io/alfinternet/baseimage-alpine:latest
```