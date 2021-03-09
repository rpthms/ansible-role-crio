# Ansible Role: CRI-O 

An Ansible Role that installs [CRI-O](https://cri-o.io/) on Linux.

Inspired by @geerlingguy's [ansible-role-containerd](https://github.com/geerlingguy/ansible-role-containerd/)

## Supported OSs

- Debian 10
- Ubuntu 18.04
- Ubuntu 20.04
- CentOS 7
- CentOS 8

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    crio_package: cri-o 
    crio_package_state: present

Package name and state controls.

    crio_service_state: started
    crio_service_enabled: true

Service controls. You can install containerd but not have it running or enabled on boot by changing these defaults.

    kubic_apt_ignore_key_error: true

Disable errors from apt-key when installing the repository key

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - rpthms.crio 
```

## License

MIT / BSD
