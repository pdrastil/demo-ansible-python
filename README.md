# Ansible demo playbook for IaaS

This repository contains demo Ansible playbook that will install
Nginx as reverse proxy with SSL and Flask demo application.

## Setup
- Install ansible via pip `pip install ansible`
- Add your hosts to `inventory/hosts` in `webservers` group.
- Ensure Ansible can connect to given hosts with account that can become root.

## Supported platforms
Following platforms have been tested during development.

- CentOS 7
- Debian 10 (Buster)
- Ubuntu 18.04 (Bionic Beaver)

## Usage
To deploy demo application run following:

```sh
$ ansible-playbook deploy.yml
```

> **NOTE:** Default configuration uses FQDN of provisioned server to setup Nginx server record.
> If not properly configured you might need to modify `server_name` variable in `inventory/group_vars`.

## Ansible role testing
Roles are testable with [Molecule](molecule.readthedocs.io) framework.

To run tests locally for given role install Docker and run:

```sh
$ pip install molecule docker
$ cd roles/nginx
$ molecule test
```

