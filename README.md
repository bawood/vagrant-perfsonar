# Vagrant/Ansible for setting up for perfsonar-pscheduler dev VM
1. Install Dependencies:
  * git - https://git-scm.com/downloads
  * Oracle VirtualBox - https://www.virtualbox.org/wiki/Downloads
  * Vagrant - https://www.vagrantup.com/downloads.html
  * vagrant-vbguest - https://github.com/dotless-de/vagrant-vbguest
  * Ansible - http://docs.ansible.com/ansible/latest/intro_installation.html#installing-the-control-machine
2. ```git clone https://github.com/perfsonar/pscheduler```
2. ```git clone https://github.com/bawood/vagrant-perfsonar```
2. ```cd vagrant-perfsonar && vagrant up```

# wait & test: 
  * when you get a shell prompt again
```
./vagrant-perfsonar$ vagrant ssh
```
```
[vagrant@localhost ~]$ pscheduler task idle --duration PT5S
Submitting task...
Task URL:
https://localhost.localdomain/pscheduler/tasks/705228e4-8810-4ba9-b2a5-93057cf3d5a3
Running with tool 'snooze'
Fetching first run...

Next scheduled run:
https://localhost.localdomain/pscheduler/tasks/705228e4-8810-4ba9-b2a5-93057cf3d5a3/runs/636bab31-542d-49ea-ae6c-3bcd7e54d0f5
Starts 2017-09-25T19:53:40Z (~7 seconds)
Ends   2017-09-25T19:53:45Z (~4 seconds)
Waiting for result...

Duration ... PT5S

No further runs scheduled.
[vagrant@localhost ~]$
```
