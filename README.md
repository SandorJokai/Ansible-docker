![npm package](https://img.shields.io/badge/ubuntu-16.04.6-purple.svg)
![npm package](https://img.shields.io/badge/ansible-2.9.23-black.svg)
![npm package](https://img.shields.io/badge/python-2.7.12-blue.svg)
![npm package](https://img.shields.io/badge/openssh-7.2p2-yellow.svg)


Ansible
------------------------------------------------------------------------
Ansible is an open-source software provisioning, configuration management, and application-deployment tool. It runs on many
Unix-like systems, and can configure both Unix-like systems as well as Microsoft Windows...

source: [wikipedia-ansible](https://en.wikipedia.org/wiki/Ansible_(software))

<h2>Prerequisites</h2>

  - working ssh connection (apt install openssh-server)
    with a key-based authentication to the managed servers (ssh-copy-id -i ~/.ssh/id_rsa.pub root@"servername")
    with root permissions enabled 
    <h6>note: if there's no id_rsa* create it first: *ssh-keygen*</h6>
    
  - python 2.7 AND/OR python 3.5 must be installed

  - must be added the hostname and IP's in to /etc/hosts file

  - In my case, I also use inside the main ansible project directory (e.g./home/user/ansible) a hosts file with
    the followings:
    *"servername" ansible_host=192.168.1.10 ansible_port=22 ansible_user=root*

------------------------------------------------------------------------
INSTALL ANSIBLE:

source: [install ansible](https://computingforgeeks.com/how-to-install-ansible-awx-on-debian-buster/)

<h1>Steps of installing</h1>

<h3>step 1: add ansible repository</h3>

- *sudo apt update*
- *echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu bionic main" | sudo tee /etc/apt/sources.list.d/ansible.list*

<h3>step 2: install gnupg for sign the repository</h3>

- *sudo apt install -y gnupg2*

<h3>step 3: implement the ansible repository public key</h3>

- *sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367*

<h3>step 4: update the repositories in order to install ansible</h3>

- *sudo apt update*

<h3>step 5: finally let's install ansible</h3>

- *sudo apt install -y ansible*

<h3>Check the version:</h3>

- *ansible --version*

------------------------------------------------------------------------
<h4>check the connection</h4>

*ansible "servername" -m ping*

Have fun and have a nice play with playbooks! :)

![npm package](https://img.shields.io/badge/ubuntu-16.04.6-purple.svg)
![npm package](https://img.shields.io/badge/ansible-2.9.23-black.svg)
![npm package](https://img.shields.io/badge/python-2.7.12-blue.svg)
![npm package](https://img.shields.io/badge/openssh-7.2p2-yellow.svg)
