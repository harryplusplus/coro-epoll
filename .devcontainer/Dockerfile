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
    # Use xdg-open to forward URLs to the host system.
    xdg-utils \
    # Use pipx to install cmake-format.
    pipx \
    && apt clean && \
    rm -rf /var/lib/apt/lists/* && \
    ln -s /usr/bin/lldb-vscode-14 /usr/bin/lldb-dap

USER vscode
RUN pipx ensurepath && \
    pipx install cmakelang
RUN echo 'alias ll="ls -a -p -lh"' >> ~/.bashrc

WORKDIR /work
