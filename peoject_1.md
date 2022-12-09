# LAMP STACK IMPLEMENTATION ON AWS

## Step 1
### Update the linux package repository
`sudo apt update`

.
	![image](./images/sudo_apt_update.png)

## Step 2
### Run Apache2 package installation
`sudo apt install apache2`

.
	![image2](./images/sudo_apt_install_apache2.png)

## Step 3
### Verify the status of apache2
`sudo systemctl status apache2`

.
	![image3](./images/sudo_systemctl_status_apache2.png)

Note: *if it shows green and 'active (running)' then you're on track*

## Step 4
### Confirm you can reach the apache server
 - Type the code below in the terminal to reveal your public ip address

 `http://169.254.169.254/latest/meta-data/public-ipv4`

 - Open any browser of your choice and type in the address bar the <public_ip_address:80>   e.g. `52.15.25.112:80` and hit enter.

You should see the Apache page as shown in the image below

![image4](./images/apache_page.png)

*If you see the following page, then your webserver is now correctly installed and accessible through your firewall.*