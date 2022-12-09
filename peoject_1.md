# LAMP STACK IMPLEMENTATION ON AWS

## Step 1 [Install Apache Server]
### Update the linux package repository
`sudo apt update`

![image](./images/sudo_apt_update.png)

## Next
### Run Apache2 package installation
`sudo apt install apache2`

![image2](./images/sudo_apt_install_apache2.png)

## Next
### Verify the status of apache2
`sudo systemctl status apache2`

![image3](./images/sudo_systemctl_status_apache2.png)

Note: *if it shows green and 'active (running)' then you're on track*

## Next
### Confirm you can reach the apache server
 - Type the code below in the terminal to reveal your public ip address

 `http://169.254.169.254/latest/meta-data/public-ipv4`

 - Open any browser of your choice and type in the address bar the <public_ip_address:80>   e.g. `52.15.25.112:80` and hit enter.

You should see the Apache page as shown in the image below

![image4](./images/apache_page.png)

*If you see the following page, then your webserver is now correctly installed and accessible through your firewall.*

## Step 2 [Install MySQL Database]
### Run the following codes on the terminal
`sudo apt install mysql-server`

![image5](./images/sudo_apt_install_mysql-server.png)
### Next login to MySQL console by typing the code
`sudo mysql`

*This will connect to the MySQL server as the administrative database user root, which is
inferred by the use of sudo when running this command. You should see output like this:*

![image6](./images/sudo_mysql.png)

it’s recommended that you run a security script that comes pre-installed with MySQL.
This script will remove some insecure default settings and lock down access to your
database system. Before running the script, you will set a password for the root user using mysql_native_password as default authentication method. We’re defining this
user’s password as PassWord.1
### Run the code below to set the password 

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'PassWord.1';`

### Next exit MySQL by typing `exit` ans hit enter to exit MySQL console

### Next is securing the securing MySQL installation by running the interactive script below

`sudo mysql_secure_installation`

![image6](./images/mysql_secure_installation1.png)
![image7](./images/mysql_secure_installation2.png)
When you’re finished, test if you’re able to login to the MySQL console by typing:
`sudo mysql-p`
Notice the -p flag in this command, which will prompt you for the password used after changing the root user password.

![image8](./images/mysql-p.png)
To exit the MySQL console, type: `exit`

## Step 3 [Installing  PHP]
`PHP` is the component of our setup that will process code to display
dynamic content to the end user. In addition to the php package, you’ll need `php-mysql`,
a PHP module that allows PHP to communicate with MySQL-based databases.You’ll also need `libapache2-mod-php` to enable Apache to handle PHP files. Core PHP
packages will automatically be installed as dependencies.
To install these 3 packages at once, run:

`sudo apt install php libapache2-mod-php php-mysql`

![image9](./images/sudo_apt_install_php_libapache2-mod-php_php-mysql.png)

