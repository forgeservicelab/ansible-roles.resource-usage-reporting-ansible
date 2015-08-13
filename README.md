Resource-usage-reporting-ansible
=========

This role deploys a resource-usage-reporting application.

Requirements
------------

iaas database and connections to it are enabled and schema is created as defined in ./files/iaas.sql. Either use the existing remote db server or use ansible-postgresql module to create it in the local server.

Role Variables
--------------

See ./defaults/main.yml for variables and set them in your master playbook.

Example Playbook
----------------

    # ./development (inventory)
	[reporting]
	193.166.25.75 ansible_ssh_user=ubuntu


    # ./reporting.yml (master playbook)
	- hosts: reporting
	  sudo: True
	  roles:
	  - resource-usage-reporting-ansible

    # Usage
	$ ansible-playbook -i development reporting.yml

License
-------

MIT

Author Information
------------------

Pasi Kivikangas, DIGILE Ltd.

