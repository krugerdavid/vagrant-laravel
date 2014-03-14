# Vagrant Laravel stack

The idea is for developers to fork this and add additional software and configuration that suits the needs of their laravel project.

## Requirements
* [VirtualBox](https://www.virtualbox.org)
* [Vagrant 1.4](http://www.vagrantup.com/download-archive/v1.4.0.html)
* [Berkshelf](http://berkshelf.com)

`gem install berkshelf`

* [vagrant-berkshelf](https://github.com/riotgames/vagrant-berkshelf)

`vagrant plugin install vagrant-berkshelf`

* [vagrant-hostmanager](https://github.com/smdahlen/vagrant-hostmanager)

`vagrant plugin install vagrant-hostmanager`

## Inital setup

After Vagrant is installed, pop open your terminal to verify it’s installed. You can do this simply by typing this in your terminal

`vagrant -v`

You can download separately the Ubuntu 12.04 box used in this example for quick sharing between your team mates and avoiding the need for each member to download the 300mb file

[Precise32](http://files.vagrantup.com/precise32.box)

After downloading this file and installed correctly vagrant on your computer, you need to do the following command

`vagrant box add precise32 /path/to/the/box/precise32.box`

Clone this repository

    $ git clone git@github.com:krugerdavid/vagrant-laravel.git project-folder

Place your website in the `./project-folder` root folder

## Usage
Start the VM

	$ cd project-folder
	$ vagrant up

## Laravel Install

	$ composer install

You will be able to run on your current folder without doing `vagrant ssh` 

You can now access your project at [http://projectname.local](http://projectname.local)

You can access remotely the mysql using for example sequelpro

![Screenshot of up-and-running mysql-server](http://content.screencast.com/users/davidkruger/folders/Jing/media/2e152cd2-8cf0-49f1-b1fd-e39482694d01/00000087.png)


## Optional configuration

If you want to change the projectname for your browser access, just change on the vagrantfile. There you can change the password for the mysql as well

## Installed software
* Apache 2
* MySQL
* PHP 5.4 (with mysql, curl, mcrypt, memcached, gd)
* memcached
* postfix
* vim, git, screen, curl, composer

## Default credentials
### MySQL
* Username: root
* Password: root
* Host: localhost
* Port: 3306

**Note:** Remote MySQL access is enabled by default, so you can access the MySQL database using your favorite MySQL client with the above credentials (and using e.g. *projectname.local* as hostname).

### Memcached
* Port: 11211
