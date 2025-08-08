FROM mcr.microsoft.com/devcontainers/base:debian-12

ENV DEBIAN_FRONTEND=noninteractive

SHELL ["/bin/bash", "-c"]

RUN apt update && \
    apt install -y \
    curl \
    git \
    build-essential \
    gdb \
    binutils \
    clang \
    lldb \
    clangd \
    cmake \
    ninja-build \
    valgrind \
    linux-perf \
    # To open in a browser on the host
    xdg-utils \
    && apt clean && \
    rm -rf /var/lib/apt/lists/* && \
    ln -s /usr/bin/lldb-vscode-14 /usr/bin/lldb-dap

USER vscode
RUN echo 'alias ll="ls -a -p -lh"' >> ~/.bashrc

WORKDIR /work
