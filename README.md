Ansible nginx playbook
======================

Ansible playbook for a simple Nginx server for HTML.

Installation
============
First things first, we'll need to get Vagrant rolling.  If you don't have it, [download Vagrant](http://downloads.vagrantup.com/) and install it for your platform.

Next thing is to boot up our Vagrant install:

`
vagrant up
`

Now we have an Ubuntu 12.04 distro running!  Now if we don't have [Ansible](http://www.ansibleworks.com) installed, [follow the instructions](http://www.ansibleworks.com/docs/intro_installation.html) or [install using pip](https://pypi.python.org/pypi/pip):


        sudo easy_install pip
        sudo pip install ansible

Change directory into the `playbooks` directory and run the following command

        % ansible-playbook -i hosts setup-nginx.yml

After running the playbook, you'll have a new host running on `192.168.111.222` with an HTTP server running ready to serve content from the `www/` directory in the root of this repository.  If you'd like to change the IP address you'll edit the hosts file within `playbooks/` and the `web.vm.network` setting.