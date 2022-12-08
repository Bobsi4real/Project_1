# LAMP STACK IMPLEMENTATION ON AWS

## Step 1
### Update the linux package repository
`sudo apt update`
	![image](./images/sudo_apt_update.png)

## Step 2
### Run Apache2 package installation
`sudo apt install apache2`
	![image2](./images/sudo_apt_install_apache2.png)

## Step 3
### Verify the status of apache2
`sudo systemctl status apache2`
	![image3](./images/sudo_systemctl_status_apache2.png)

Note: *if it shows green and 'active (running)' then you're on track*

## Step 4
### Confirm you can reach the apache server