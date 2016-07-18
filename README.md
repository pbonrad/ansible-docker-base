ansible-base
============

Simple original distribution with Python installed. Can be used as a base server to provision application with Ansible.

Main use case for me was testing of my created Ansible roles on different distributions.

Usage
-----
    docker run -td --privileged --name [name] pbonrad/ansible-base:debian-7 /sbin/init

Always start the container with `--privileged` and call `/sbin/init`. Otherwise systemd is not working correctly and you are not able to install any services.

Please use `[name] ansible_connection=docker` in Ansible playbook (host) to connect to the running docker container.

Tags
----
    pbonrad/ansible-base:debian-7
    pbonrad/ansible-base:debian-wheezy
    pbonrad/ansible-base:debian-8
    pbonrad/ansible-base:debian-jessie
    pbonrad/ansible-base:ubuntu-15.10
    pbonrad/ansible-base:ubuntu-wily
    pbonrad/ansible-base:ubuntu-16.04
    pbonrad/ansible-base:ubuntu-xenial
