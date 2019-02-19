# Restart Apache 2 web server, enter:
# /etc/init.d/apache2 restart
OR
$ sudo /etc/init.d/apache2 restart
OR
$ sudo service apache2 restart

#To stop Apache 2 web server, enter:
# /etc/init.d/apache2 stop 
OR
$ sudo /etc/init.d/apache2 stop
OR
$ sudo service apache2 stop

#To start Apache 2 web server, enter:
# /etc/init.d/apache2 start
OR
$ sudo /etc/init.d/apache2 start
OR
$ sudo service apache2 start

A note about Debian/Ubuntu Linux systemd users

Use the following systemctl command on Debian Linux version 8.x+ or Ubuntu Linux version Ubuntu 15.04+ or above:
## Start command ##
systemctl start apache2.service
## Stop command ##
systemctl stop apache2.service
## Restart command ##
systemctl restart apache2.service

CentOS/RHEL (Red Hat) Linux version 4.x/5.x/6.x or older specific commands

## Start ##
service httpd start
## Stop ##
service httpd stop
## Restart ##
service httpd restart

CentOS/RHEL (Red Hat) Linux version 7.x or newer specific commands

Most modern distro now using systemd, so you need to use the following command:
## Start command ##
systemctl start httpd.service
## Stop command ##
systemctl stop httpd.service
## Restart command ##
systemctl restart httpd.service

Generic method to start/stop/restart Apache on a Linux/Unix

The syntax is as follows (must be run as root user):
## stop it ##
apachectl -k stop
## restart it ##
apachectl -k restart
## graceful restart it ##
apachectl -k graceful
## Start it ##
apachectl -f /path/to/your/httpd.conf
apachectl -f /usr/local/apache2/conf/httpd.conf
