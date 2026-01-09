FROM mcr.microsoft.com/devcontainers/python:2-${templateOption:imageVariant}

COPY --from=docker.io/astral/uv:latest /uv /uvx /bin/

RUN apt-get update && apt-get upgrade -y \
    && rm -rf /var/lib/apt/lists/*