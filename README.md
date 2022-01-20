# docker-baseimage-alpine
A custom base image built with Alpine linux and S6 overlay.


## Building locally

If you want to make local modifications to these images for development purposes or just to customize the logic:

```bash
git clone https://github.com/ALFinternet/docker-baseimage-alpine.git
cd docker-baseimage-alpine
docker build \
  --no-cache \
  --pull \
  -t ghcr.io/alfinternet/baseimage-alpine:3.15 .

docker tag <IMAGE_ID> ghcr.io/alfinternet/baseimage-alpine:latest
```