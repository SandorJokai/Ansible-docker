<h2>Usage</h2>

```bash
ansible-playbok playbook.yml
```

There are only 4 lines in playbook.yml...

The way how ansible works is based on searching for files basically. Ansible will examine *playbook.yml* for first. There are *roles* section in that file. It will be searched for more information in *apache* directory where this name matched with the name of *role*. In *apache* there more directories, but ansible will continue in *tasks* directory. 
*Tasks* is another main directory, the rest just consist of configfiles and variables, etc.

So the basic playbook will work from [/apache/tasks/main.yml](https://github.com/SandorJokai/Ansible-docker/blob/master/apache-install/apache/tasks/main.yml)
