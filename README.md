# Ansible-Sandbox
Ansible sandbox using vagrant

# Need Vagrant/VirtualBox
You have to install Vagrant to try this on your local machine https://developer.hashicorp.com/vagrant/downloads <br>
You need VirtualBox https://www.virtualbox.org <br>

# Initialisation
To start VM use `vagrant up` <br>
See the machine name ? `vagrant status`<br>
To connect VM use `vagrant ssh {VmName}` (vm name is in vagrantfile and when you up can see the name) <br>
create user on every machine `sudo adduser ansible` and add it on sudoers file `sudo visudo` and add `ansible ALL=(ALL) NOPASSWD:ALL` and connect ansible user for `sudo chmod 777 .ssh`<br>
create ssh key on ansibleVM `ssh-keygen -t rsa` and send it to all vm Master/Worker for the installation package `sudo ssh-copy-id -i /home/vagrant/.ssh/id_rsa.pub ansible@192.168.50.{ipvm}`<br>
<br>
AFTER THAT ENJOY ;) !<br>

# Machine
<b>Ansible</b> 192.168.50.10        <br>
<b>Master</b>  192.168.50.11        <br>
<b>Worker</b>  192.168.50.12-254    <br>


## AnsibleVM
This machine have ansible and connection ssh for all other machine

## Master
This machine is the Master cluster Docker Swarm or Kubernetes