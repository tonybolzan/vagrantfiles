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
# If you have mDNS (default on Mac OS X and Ubuntu), access in:
# http://example.local/
# Or, add entry to your hosts
sudo echo "192.168.50.2 example.local" >> /etc/hosts
# Enjoy
```
**PS.:** If your project have a directory `php`, `public`, `public_html`, `web` or `www` inside of a directory specified in variable `folder` in `Vagrantfile`, it will be used as Document Root of the Web Server.
Otherwise the variable `folder` will be assumed.

## Settings
You can modify Vagrantfile for your requirements, The default settings are:
```ruby
hostname = "example.local"	# Internal hostname for machine and name of the machine in Virtualbox
address  = "192.168.50.2"	# Private IP address of the machine
folder   = "./"				# The shared folder is the same as the current folder Vagrantfile
forward  = false			# Forward ports from guest to host
```

### PHP Xdebug
Set your IDE key to `VAGRANT`.

### PHP XHProf
To access xhprof go to:
`http://example.local/xhprof/`

## Changelog
### 2014/09/17
- Support mDNS and changed domain `.dev` to `.local`
### 2014/06/02
- Autodetect NGINX Document Root in `$folder/php/`, `$folder/public/`, `$folder/public_html/`, `$folder/web/`, `$folder/www/`, `$folder/`


# LAMP Stack

## Packages
- Debian 7.5 Wheezy
- Apache HTTPD
- PHP 5.5 + Xdebug + XHProf
- MySQL 5.6
- MongoDB 2.6

## Usage
Same as LEMP Stack, but change `LEMP` to `LAMP`
