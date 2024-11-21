# Use the official Ubuntu 22.04 image from Docker Hub
FROM ubuntu:22.04

# Update and install necessary packages
RUN apt-get update && apt-get install -y \
    sudo \
    build-essential \
    git \
    libncurses-dev \
    bison \
    flex \
    libssl-dev \
    libelf-dev \
    vim \
    acl \
    whiptail \
    locales \
    uuid-runtime \
    libmpc-dev \
    wget \
    curl \
    && apt-get clean

RUN useradd -m docker && echo "docker:docker" | chpasswd && adduser docker sudo

USER docker

# Set the working directory
WORKDIR /mnt/dm3588

# Default command to display the kernel version
CMD ["/bin/bash"]

