# Dependencies
- [Virtualbox 4.3.10](https://www.virtualbox.org/wiki/Downloads)
- [Virtualbox Extension Pack](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant >= 1.5.0](http://www.vagrantup.com/downloads.html)

# LEMP Stack

## Packages
- Debian 7.5 Wheezy
- Nginx 1.6
- PHP 5.5 + FPM + Xdebug + XHProf
- MySQL 5.6
- MongoDB 2.6

## Usage
```bash
# Go to Your Project
cd your/project/
# Get Vagrantfile
curl -sS 'https://raw.githubusercontent.com/tonybolzan/vagrantfiles/master/LEMP/Vagrantfile' > Vagrantfile
# Edit Vagrantfile Settings (Description Below)
vim Vagrantfile
# Start Machine
vagrant up
# Add entry to your hosts
sudo echo "192.168.50.2 example.dev" >> /etc/hosts
# Enjoy
```
**PS.:** Your project must have a `public_html` directory under the `folder` specified in Vagrantfile.
If you want to modify this behavior, please download the `Vagrantshell`, modify the configuration of Nginx in the parameter `root`.
If a "Vagrantshell" exists in the same path that "Vagrantfile" it will be used, otherwise it will be downloaded from github.


## Settings
You can modify Vagrantfile for your requirements, The default settings are:
```ruby
hostname = "example.dev"	# Internal hostname for machine and name of the machine in Virtualbox
address  = "192.168.50.2"	# Private IP address of the machine
folder   = "./"				# The shared folder is the same as the current folder Vagrantfile
forward  = false			# Forward ports from guest to host
```

### PHP Xdebug
Set your IDE key to `VAGRANT`.

### PHP XHProf
To access xhprof go to:
`http://example.dev/xhprof/`