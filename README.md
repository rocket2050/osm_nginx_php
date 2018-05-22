Osm_Nginx_PHP
=========

Ansible role of PHP and php-fpm for RedHat and Debian Family. By default this will install and configure php version 5.6.

Requirements
------------
The only requirment is python-common-software-properties in Debian based Operating System and libselinux-python in redhat6.

extra-vars
==========

The role contains multi domain support where by providing php version in variable you can customise the version want to install.

Example for custome vars:  

redhat
-------  
```
--extra-vars php=56/71

eg: for php7.1  
ansible-playbook --extra-vars php=71 site.yml
```

debian  
------- 
``` 
--extra-vars php_version=7.1

eg: ansible-playbook --extra-vars php_version=7.1 site.yml
```

Role Variables
--------------
The role variables are in [vars](https://github.com/opstree-ansible/osm_nginx_php/blob/master/vars/main.yml)

Dependencies
------------

There is no any special dependency

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: "{{ hosts }}"
      roles:
         - { role: osm_nginx_php }
Verify
------
http://ip/info.php
