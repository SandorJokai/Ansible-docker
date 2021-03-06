![npm package](https://img.shields.io/badge/ubuntu-16.04.6-purple.svg)
![npm package](https://img.shields.io/badge/ansible-2.9.23-black.svg)
![npm package](https://img.shields.io/badge/python-2.7.12-blue.svg)
![npm package](https://img.shields.io/badge/openssh-7.2p2-yellow.svg)


<h2>Ansible</h2>

Ansible is an open-source software provisioning, configuration management, and application-deployment tool. It runs on many
Unix-like systems, and can configure both Unix-like systems as well as Microsoft Windows...

source: [wikipedia-ansible](https://en.wikipedia.org/wiki/Ansible_(software))

<h2>Prerequisites</h2>

  - established ssh connection between the host and the managed clients
    Only work with root privileges.
  ```bash
  ssh-copy-id -i ~/.ssh/id_rsa.pub root@"servername"
  ```
  
  <h6>note: if there's no id_rsa* create it first:</h6>
  
  ```bash
  ssh-keygen
  ```
    
  - python 2.7 AND/OR python 3.5 must be installed

  - must be added the hostname and IP's in to /etc/hosts file

------------------------------------------------------------------------
<h2>Install Ansible</h2>

How to install in Debian10 (*buster*)

source: [install ansible](https://computingforgeeks.com/how-to-install-ansible-awx-on-debian-buster/)

<h1>Steps of installing</h1>

<h3>step 1: add ansible repository</h3>

```bash
sudo apt update
echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu bionic main" | sudo tee /etc/apt/sources.list.d/ansible.list
```

<h3>step 2: install gnupg for sign the repository</h3>

```bash
sudo apt install -y gnupg2
```

<h3>step 3: implement the ansible repository public key</h3>

```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
```

<h3>step 4: update the repositories in order to install ansible</h3>

```bash
sudo apt update
```

<h3>step 5: finally let's install ansible</h3>

```bash
sudo apt install -y ansible
```

<h3>step 6: edit hostfile</h3>

There's a host file in the main ansible directory (e.g./home/user/ansible), edit with the followings:
    
```bash
"servername" ansible_host=192.168.1.10 ansible_port=22 ansible_user=root
```

<h3>Check the version:</h3>

```bash
ansible --version
```

------------------------------------------------------------------------
<h4>check the connection</h4>

```bash
ansible "servername" -m ping
```

Have fun and have a nice play with playbooks! :)

![npm package](https://img.shields.io/badge/ubuntu-16.04.6-purple.svg)
![npm package](https://img.shields.io/badge/ansible-2.9.23-black.svg)
![npm package](https://img.shields.io/badge/python-2.7.12-blue.svg)
![npm package](https://img.shields.io/badge/openssh-7.2p2-yellow.svg)
