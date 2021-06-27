![npm package](https://img.shields.io/badge/ubuntu-16.04.6-purple.svg)
![npm package](https://img.shields.io/badge/docker-18.09.7-lightblue.svg)
![npm package](https://img.shields.io/badge/docker_compose-1.26.0-turquoise.svg)
![npm package](https://img.shields.io/badge/ansible-2.9.23-black.svg)
![npm package](https://img.shields.io/badge/python-2.7.12-blue.svg)
![npm package](https://img.shields.io/badge/openssh-7.2p2-yellow.svg)
![npm package](https://img.shields.io/badge/apache-2.4.38-cyklamen.svg)
![npm package](https://img.shields.io/badge/mariadb-10.3.29-red.svg)
![npm package](https://img.shields.io/badge/ampache-4.1.1-orange.svg)

<h1>Introduce the project</h1>

The concept of use this is running the well-known ampache music-streaming service on apache webserver with a mariadb
Database system behind, orchestrating with docker-compose. And the whole procedure from installing components until 
running the service is managing by an ansible playbook. I was just beginning to see the greatness of this...

official website of the free licenced (AGPLv3) [ampache](http://ampache.org/)

<h1>Prerequisites</h1>

- the managed systems is Ubuntu 16.04 x86_64 in my case
- Openssh-server must be installed
- must be configured an established connection with ansible
- must be enabled the root login via ssh (*/etc/ssh/sshd_config*)

<h3>Process time approx.: 20 min</h3>

After finished the running the playbook, check in a browser by typing the hostname of the managed machine (or it's IP's)
and ampache's welcome site will be shown.
Type the mysql's credentials which is ampache in my case (USERNAME=PASSWORD=ampache) change the mysql hostname
from localhost to db, take the tick out from DB create as it is already done and enjoy! :)

*note: It could go to an error whilst the playbook.yml last task is running, it happens when the application
server (music-streamer_web_1) could not start for first. Solve that is just run one more time the ansible-playbook playbook.yml command and everything should work just fine.
Once it's up and running, it will be even after a reboot.

<h4>Path of sample music dir for create a catalog in web:</h4>

/var/lib/docker/ampache/musics

