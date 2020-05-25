Introduce the project:
-----------------------------------------------

According to use this is running an ampache music-streaming service on apache webserver with a mariadb
Database system behind, orchestrating with docker-compose. And the whole procedure from installing components until 
running the service is managing by an ansible playbook. I was just beginning to see the greatness of this...

official website of the free licenced (AGPLv3) ampache: http://ampache.org/

Prerequisites on managed systems ( Ubuntu 16.04 x86_64 in my case ):
-----------------------------------------------
  - Openssh-server must be installed
  - must be configured an established connection with ansible
  - must be enabled the root login via ssh with modify in /etc/ssh/sshd_config
-----------------------------------------------
Process time approx.: 30 min
-----------------------------------------------
After finish running the playbook, check in a browser by typing the hostname of the managed machine (or it's IP's)
and ampache's welcome site will be showed up.
Type the mysql's credentials which is ampache in my case (USERNAME=PASSWORD=ampache) change the mysql hostname
from localhost to db, take the tick out from DB create as it is already done and enjoy! :)

Path of sample music dir for create a catalog in web:
-----------------------------------------------
/var/lib/docker/ampache/musics

