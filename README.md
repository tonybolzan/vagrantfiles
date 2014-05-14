Collection of Vagrantfiles
============

# Dependencies
- [Virtualbox 4.3.10](https://www.virtualbox.org/wiki/Downloads)
- [Virtualbox Extension Pack](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant >= 1.5.0](http://www.vagrantup.com/downloads.html)

# LEMP Stack

## Usage
```bash
# Go to Your Project
cd your/project/
# Get Vagrantfile
curl 'https://raw.github.com/tonybolzan/vagrantfiles/master/LEMP-Stack/Vagrantfile' > Vagrantfile
# Edit Vagrantfile Settings
vim Vagrantfile
# Start Machine
vagrant up
# Add entry to your hosts
sudo echo "192.168.50.2 example.dev" >> /etc/hosts
# Enjoy
```

## Packages
Debian 7.5 Wheezy
Nginx 1.6
PHP 5.5 + FPM
MySQL 5.6

### You can modify Vagrantfile for your requirements, The default settings are:
```ruby
hostname = "example.dev"	# Internal hostname for machine and name of the machine in Virtualbox
address  = "192.168.50.2"	# Private IP address of the machine
folder   = "./"				# The shared folder is the same as the current folder Vagrantfile
remote   = true				# The install script should be obtained from github or locally in Vagrantshell
forward  = false			# Forward ports from guest to host
```

#### OBS.: Your project must have a `public_html` directory under the `folder` specified in Vagrantfile.
