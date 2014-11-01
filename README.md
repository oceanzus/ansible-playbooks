ansible-playbooks
=================

A repository of ansible-playbooks for deploying remote instances and common deployment strategies

Setting Up
====

#### Create a hosts file in the playbook

`roles/hosts`
```txt
[dev]
# An Amazon AMI host
192.168.1.12
```

#### Set your SSH Configure

Ansible can rely on your SSH configuration to connect to a specified host using the appropriate settings. This allows you to connect to hosts that require an identity file, or a non-standard port.

`~/.ssh/config`
```txt
Host dev
    HostName dev
    User ec2-user
    IdentityFile ~/.ssh/AWS.pem
```

Using a Playbook
===

```shell
cd playbook
ansible-playbook -i hosts <play>.yml
```

Our Playbooks
===

- Python 2.7
- NetCDF
