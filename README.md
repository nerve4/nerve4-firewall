# firewall

An Ansible role that install/manage firewalls to CENTOS 7/8, Rocky9 and Ubuntu.


## Requirements

Make sure, you made your vars file with valid path to custom template or you can use Default vars.

You need `ansible 2.13.7` to run this module

The `ansible.posix.firewalld` module [module](https://docs.ansible.com/ansible/latest/collections/ansible/posix/firewalld_module.html) and The Role also use `community.general collection` module. To install it, use: `ansible-galaxy collection install community.general`. is also necessary.

## Tasks descriptionsa

- main.yml - Run the OS check and run the relevant playbook
- rhel-install-firewalld.yml - Deploy firewalld on Rhel
- run-config-firewalld.yml - Configure firewalld on Rhel
- run-config-ufw.yml - Configure ufw on Ubuntu
- ubuntu-install-ufw.yml - Deploy ufw on Ubuntu


## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: servergroup
  become: true
  become_user: lee

  vars_files:
    - vars/main.yml
    
  roles:
    - nerve4-firewall
```

## Maintainer Information
Lee | 2023