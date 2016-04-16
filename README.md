### Wordpress Ansible Playbook

Tested with:

```
$ ansible --version
ansible 2.1.0 (devel 50dfd4b057) last updated 2016/02/07 13:39:55 (GMT +900)
  lib/ansible/modules/core: (detached HEAD e1ec52e365) last updated 2016/02/07 13:41:53 (GMT +900)
  lib/ansible/modules/extras: (detached HEAD 14a62fb5d6) last updated 2016/02/07 13:42:45 (GMT +900)
  config file =
  configured module search path = Default w/o overrides
```

### Usage

1. replace `hosts.example`, `vars_secret.yml.example`, `vars_main.yml.example` with real ones.

2. run commands as below:

```
# make sure ssh connection is fine
$ ansible -i hosts -u ubuntu -l production all -m ping

# run playbook
$ ansible-playbook -i hosts -l production playbook.yml
```

### Try with Vagrant

```
# launch VM
$ vagrant up

# make sure ssh connection is fine
$ ansible -i hosts -u ubuntu -l vagrant all -m ping

# run playbook
$ ansible-playbook -i hosts -l vagrant playbook.yml
```
