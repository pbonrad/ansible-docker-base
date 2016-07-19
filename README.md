ansible-docker-base
===================

Dockerfiles with original distribution as the base image and Python installed. Can be used as a base server to provision applications with Ansible.

Main use case for me was testing of my created Ansible roles on different distributions and versions.

Usage
-----
    docker run -td --privileged --name [name] pbonrad/ansible-docker-base:debian-7

Always start the container with `--privileged`, otherwise systemd is not working correctly and you are not able to install any services.

Please use `[name] ansible_connection=docker` in Ansible playbook (host) to connect to the running docker container.
