# ASCN-TP

## Prerequisites
in order to follow these steps you need to install `vagrant`(https://www.vagrantup.com/docs/installation) and `ansible` (https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)


## Setup
First go to the project dir and then run vagrant up to create the virtual machine if it's not created
```bash
❯ vagrant up
```

Check if the vm is running with vagrant status
```bash
❯ vagrant status
Current machine states:

wikijs                    running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.

```

After that run the ansible-playbook command

```bash
❯ ansible-playbook playbook.yaml -i hosts -u vagrant --private-key .vagrant/machines/wikijs/virtualbox/private_key
```

Last but not least

Go to the browser and type the ip address of the virtual machine `172.17.177.42`
