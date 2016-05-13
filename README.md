# StompVM

A virtual machine for developing software for Stompy.
Written using Vagrant + Ansible.


## Install prereqs

Consistency is hard.  A development environment for a robot should
Get Vagrant, Virtualbox, and Ansible installed


### Virtualbox

In Debian-based linux:

    sudo apt install virtualbox


### Vagrant

In Debian-based linux:

    sudo apt install vagrant


### Ansible

Ansible is available in Debian-based linux from jessie-backports on

    apt install -t jessie-backports ansible

The ROS package provided by jalessio needds to be installed:

    ansible-galaxy install jalessio.ROS


## Working with the VM

### Creating

Now that everything is installed, we use `vagrant` to create and manage stompvm. 
To create the vm, run:

    vagrant up

Vagrant will download the ubuntu base image and run the ansible provisioner to configure the vm.

### Updating

If you update your copy of this repository, or edit the ansible configuration, you can re-run the provisioning step:

    vagrant provision

### Logging in

To log into the resulting machine:

    vagrant ssh
