Ansible Role: SNAP Package Install
=========

An Ansible role to install specified packages using SNAP.

Requirements
------------
This Ansible role has been developed and thoroughly tested with Ansible version 2.10.8

This role was designed for:

- Ubuntu 22.04.4 LTS (Jammy Jellyfish)

Role Variables
--------------

Example 

    package_list:
      - net-tools
      - netcat
      - iftop
      - glances
      - nfs-common
      - jq

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      become: true
      vars_files:
        - group_vars/all.yml
      roles:
        - ansible-role-snap-package-install

License
-------

MIT / BSD

🇬🇧🇭🇰 Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
