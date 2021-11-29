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

After that ssh into the created machine

```bash
❯ vagrant ssh
```

then go to the `/vagrant` dir and run the playbook

```bash
❯ ansible-playbook gcp_playbook.yaml --private-key=./your_private_key
```

**note:** you'll have to create a new ssh key and copy it to the google cloud platforn, then copy
it to the project dir and use it as `your_private_key`, otherwise it will
not work properly.
