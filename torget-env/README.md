# Ubuntu Docker for Ansible

This sets up an Ubuntu 22.04 Docker container with SSH for Ansible testing.

---

## Start container

docker run -dit --name ansible-target -p 2222:22 ubuntu:22.04

---

## Install SSH inside container

docker exec -it ansible-target bash

apt update
apt install -y openssh-server python3 sudo
mkdir -p /var/run/sshd

---

## Test SSH

 ssh user@192.168.56.3
vm has pub. kye of my macbook

---

## Cleanup

docker stop ansible-target
docker rm ansible-target