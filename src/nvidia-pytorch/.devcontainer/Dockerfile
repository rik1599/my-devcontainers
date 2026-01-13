FROM nvcr.io/nvidia/pytorch:24.06-py3

COPY --from=docker.io/astral/uv:latest /uv /uvx /bin/

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    # Remove imagemagick due to https://security-tracker.debian.org/tracker/CVE-2019-10131
    && apt-get purge -y imagemagick imagemagick-6-common \
    && apt-get upgrade -y \
    && rm -rf /var/lib/apt/lists/*