Docker
=========

This role helps install and configure Docker on Ubuntu or Centos. It will configure the docker repositories, install docker prerequisites, and do some minor configurations.

Requirements
------------

This role requires Ansible 2.4 or upper.

Role Variables
--------------

Availables variables are described below, including any variables that are in defaults/main.yml:

```yaml
# defaults file for synehan.docker
# Proxy configuration
docker_use_proxy: False
docker_http_proxy: ""
docker_https_proxy: ""
docker_no_proxy: ""

# If you want to use this role with an old installation.
docker_remove_old_packages: False

# Activate Edge and Test repositories (Only for Centos)
docker_edge_repository_enable: no
docker_test_repository_enable: no

# The version of docker you want to use. For example
# On Centos: 17.09.1.ce
# On Ubuntu: 17.09.1~ce-0~ubuntu
docker_version: ""

# Enable debug
docker_daemon_config_debug: 'false'
docker_daemon_config_log_level: 'debug'
```

Dependencies
------------

None.

Example Playbook
----------------

You can simply use this role like this: 

    - hosts: servers
      roles:
         - { role: synehan.docker }

License
-------

BSD

Author Information
------------------
