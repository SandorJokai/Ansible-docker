                                 ------------- INTRODUCE THE PROJECT: -------------

The final manifestation of this is running an ampache music-streaming service on apache webserver with a mariadb
DB system behind, orchestrating with docker-compose. And the whole procedure from installing components until run-
ning the service is managing by an ansible playbook. I was just beginning to see the greatness of this...
-----------------------------------------------
Prerequisites on managed systems ( Ubuntu 16.04 x86_64 in my case ):
  - Openssh-server must be installed
  - must be configured an established connection with ansible
  - must be enabled the root login via ssh with modify in /etc/ssh/sshd_config
-----------------------------------------------
After finish running the playbook, check in a browser by typing the hostname of the managed machine (or it's IP's)
and ampache's welcome site will be showed up.
Type the mysql's credentials which is ampache in my case (USERNAME=PASSWORD=DATABASE) change the mysql access
for db and enjoy! :)
