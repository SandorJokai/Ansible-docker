Ansible
------------------------------------------------------------------------
Ansible is an open-source software provisioning, configuration management, and application-deployment tool. It runs on many
Unix-like systems, and can configure both Unix-like systems as well as Microsoft Windows...

source: https://en.wikipedia.org/wiki/Ansible_(software)

Prerequisites:

  - working ssh connection (apt install openssh-server)
    with a key-based authentication to the managed servers (ssh-copy-id -i ~/.ssh/id_rsa.pub root@"servername"
    with root permissions enabled
  - python 2.7 AND/OR python 3.5 must be installed
  - must be added the hostname and IP's in to /etc/hosts file
    In my case, I also use inside the main ansible project directory a hosts file with the followings:
    "servername" ansible_host=192.168.1.10 ansible_port=22 ansible_user=root
    .
    .
    .
------------------------------------------------------------------------
INSTALL ANSIBLE:

sudo apt update
  Add Ansible APT repository ---> echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu bionic main" | sudo \
                                  tee /etc/apt/sources.list.d/ansible.list
sudo apt install -y gnupg2\
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367\
sudo apt update
sudo apt install -y ansible
ansible --version

------------------------------------------------------------------------
Let's check the connection is ready with root permission:
ansible "servername" -m ping

Have fun and have a nice play with playbooks! :)
