# Install and configure Docker SWARM on Vagrant using ansible.

Vagrant is a tool for building and distributing development environments.

Development environments managed by Vagrant can run on local virtualized
platforms such as VirtualBox or VMware, in the cloud via AWS or OpenStack,
or in containers such as with Docker or raw LXC.

Vagrant provides the framework and configuration format to create and
manage complete portable development environments. These development
environments can live on your computer or in the cloud, and are portable
between Windows, Mac OS X, and Linux.



## Quick Start

For the quick-start, we'll bring up a development machine on
[VirtualBox](https://www.virtualbox.org/) because it is free and works
on all major platforms.
First, make sure your development machine has
[VirtualBox](https://www.virtualbox.org/)
installed. After this,
[download and install the appropriate Vagrant package for your OS](https://www.vagrantup.com/downloads.html).

To build your first virtual environment:

Clone the git repo [https://github.com/pprashanth/vagrant_docker_anisble](https://github.com/pprashanth/vagrant_docker_anisble) .
Go to the cloned repo directory .You will find two files ,

  1.vagrant - This is  a simple vagrant file which spins up Virtual boxes for you .
  2.playbook.yml -  This is anisible playboox runs on Virtual boxes and install required packages for you.Modify this file  incase you need additioanl packages.


```bash
    vagrant up
    Vagrant status
```

