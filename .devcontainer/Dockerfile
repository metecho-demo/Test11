# Use the latest version of the d2x image
FROM ghcr.io/metecho-demo/d2x:latest

# Set environment variables
ENV DEBIAN_FRONTEND=noninteractive
ENV SF_CONTAINER_MODE=true
ENV SHELL=/bin/bash

# Set up bash prompt
USER d2x
COPY .devcontainer/pureline.conf ~/pureline.conf
RUN git clone https://github.com/chris-marsh/pureline.git ~/pureline && \
    echo 'if [ "$TERM" != "linux" ]; then\n    source ~/pureline/pureline ~/.pureline.conf\nfi' >> ~/.bashrc