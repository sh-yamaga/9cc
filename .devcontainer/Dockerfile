FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

RUN apt update && apt upgrade -y
RUN DEBIAN_FRONTEND=noninteractive apt install -y gcc make git binutils libc6-dev gdb sudo || apt-get install -y --fix-missing gcc make git binutils libc6-dev gdb sudo
RUN apt clean
RUN adduser --disabled-password --gecos '' user
RUN echo 'user ALL=(root) NOPASSWD:ALL' > /etc/sudoers.d/user
USER user
WORKDIR /home/user