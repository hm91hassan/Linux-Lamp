# Linux-Lamp
Install Linux, Apache, MySQL, PHP (LAMP) stack on Ubuntu 18.04

Step 1 — Installing Apache and Updating the Firewall

sudo apt update
sudo apt install apache2

sudo ufw app list

sudo ufw app info "Apache Full"

sudo ufw allow in "Apache Full"

sudo apt install curl
curl http://icanhazip.com

Step 2 — Installing MySQL

sudo apt install mysql-server
sudo mysql_secure_installation
Answer Y for yes, or anything else to continue without enabling.

sudo mysql
SELECT user,authentication_string,plugin,host FROM mysql.user;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
SELECT user,authentication_string,plugin,host FROM mysql.user;
exit

sudo apt install php libapache2-mod-php php-mysql
sudo gedit /etc/apache2/mods-enabled/dir.conf

sudo systemctl restart apache2
sudo systemctl status apache2
Press Q to exit this status output.
apt search php- | less
Press Q to exit this status output.

apt show php-cli
sudo apt install php-cli

