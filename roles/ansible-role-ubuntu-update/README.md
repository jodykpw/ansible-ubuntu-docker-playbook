Ansible Role: Update
=========

Ansible role for system updates

This role provides a streamlined and automated way to perform system updates on target hosts using Ansible. It ensures that the latest software packages, security patches, and system updates are applied to the target systems, helping to maintain their stability, security, and compatibility.

Requirements
------------

This Ansible role has been developed and thoroughly tested with Ansible Core version 2.15.0.

This role was designed for:

- Ubuntu 22.04.4 LTS (Jammy Jellyfish)

Role Variables
--------------

If true, remove unused dependency packages for all module states except build-dep. It can also be used as the only option.

    update_autoremove: false

apt_upgrade type which can be: dist, full, yes, or safe
    
    update_upgrade_command: dist

Update the apt cache if it is older than the cache_valid_time. This option is set in seconds.

    update_cache_valid_time: 1

Option to exclude certain packages or package groups from being updated during a system update process.

    # Names specific packages from being updated.
    # Example
    # update_excluded_packages:
    #   - kernel*
    #   - docker*
    #   - kube*
    update_excluded_packages: []

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      become: true
      vars:
        update_autoremove: false
        update_upgrade_command: dist
        update_cache_valid_time: 1
        update_excluded_packages: []
      roles:
        - ansible-role-update

License
-------

MIT / BSD

Author Information
------------------

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com