# ansible-ow-influxdb

[![Build Status](https://github.com/openwisp/ansible-ow-influxdb/workflows/Ansible%20OpenWISP%20InfluxDB%20CI%20Build/badge.svg?branch=master)](https://github.com/openwisp/ansible-openwisp2/actions?query=workflow%3A%22Ansible+OpenWISP+Infl+CI+Build%22)

Simple ansible role for installing and configuring influxdb.

Designed to be used in OpenWISP installations.

How to run tests
----------------

If you want to contribute to `ansible-ow-influxdb` you should run tests
in your development environment to ensure your changes are not breaking anything.

To do that, proceed with the following steps:

**Step 1**: Clone `ansible-ow-influxdb`

Clone repository by:

    git clone https://github.com/<your_fork>/ansible-ow-influxdb.git

**Step 2**: Install docker

If you haven't installed docker yet, you need to install it (example for Debian/Ubuntu systems):

    sudo apt install docker.io

**Step 3**: Install molecule and dependencies

    pip install molecule[docker] yamllint ansible-lint docker

**Step 4**: Download docker images

    docker pull geerlingguy/docker-ubuntu2204-ansible:latest
    docker pull geerlingguy/docker-ubuntu2004-ansible:latest
    docker pull geerlingguy/docker-ubuntu1804-ansible:latest
    docker pull geerlingguy/docker-debian10-ansible:latest
    docker pull geerlingguy/docker-debian11-ansible:latest

**Step 5**: Run molecule test

    molecule test -s local

If you don't get any error message it means that the tests ran successfully without errors.

**ProTip:** Use `molecule test --destroy=never` to speed up subsequent test runs.

Role Variables
==============

```yaml
# By default query logging of InfluxDB is turned off since it can occupy a
# lot of storage. You can turn it on by setting below variable to true.
influxdb_query_logging: true
# The username of the influxdb user that will be created.
influxdb_user_username: admin
# The password of the influxdb user that will be created.
influxdb_user_password: "your-strong-password"
# The hostname or IP address on which InfluxDB server is listening.
influxdb_http_ip: "localhost"
# The port on which InfluxDB server is listening.
influxdb_http_port: 8086
```
