# 📕 Ansible Ubuntu Docker Playbook

An Ansible playbook designed to set up a docker server on Ubuntu 22.04.4 LTS (Jammy Jellyfish).

## 🗂️ The files structure is organised this way:
Based on [Ansible Best Practices: Sample directory layout](https://docs.ansible.com/ansible/latest/tips_tricks/sample_setup.html#sample-directory-layout)

## 🚀 Quick start

1. `git clone --recursive` this repository.
2. Go to the cloned folder.
3. Editing playbook yml, ensure set hosts correctly.
4. Editing the group_vars files, you can customize variables specific to different groups of hosts in your Ansible inventory. These variables will be applied when running playbooks or tasks that target the corresponding group of hosts.
5. Select a playbook (see [`Available playbooks`](https://github.com/truewebartisans/useful-playbooks#-available-playbooks) section).
6. Run `<playbook_name>` -i `<inventory_name>`

Example

```console
ansible-playbook init-server.yml -i hosts.ini
```

## 📚 Available playbooks

- 📖 `init-server.yml` Is an Ansible playbook designed for server initialization and configuration. 

- 📖 `docker.yml` Integrated with the [geerlingguy/ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker).

- 📖 `rsnapshot.yml` Is used to configure and manage the rsnapshot backup.

## 📄 License

MIT / BSD

## 🇬🇧🇭🇰 Author Information

* Author: Jody WAN
* Linkedin: https://www.linkedin.com/in/jodywan/
* Website: https://www.jodywan.com
