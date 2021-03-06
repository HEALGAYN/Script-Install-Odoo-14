# [Odoo](https://www.odoo.com "Odoo's Homepage") Install Script


## Installation procedure

##### 1. Update Linux:
```
sudo apt update
```
##### 2. Upgrade Linux:
```
sudo apt upgrade
```
##### 3. Download the script:
```
sudo wget https://raw.githubusercontent.com/HEALGAYN/Scripts-Install-Odoo-14/main/odoo_install_debian.sh
```
##### 4. Modify the parameters as you wish.
There are a few things you can configure, this is the most used list:<br/>
```OE_USER``` will be the username for the system user.<br/>
```GENERATE_RANDOM_PASSWORD``` if this is set to ```True``` the script will generate a random password, if set to ```False```we'll set the password that is configured in ```OE_SUPERADMIN```. By default the value is ```True``` and the script will generate a random and secure password.<br/>
```INSTALL_WKHTMLTOPDF``` set to ```False``` if you do not want to install Wkhtmltopdf, if you want to install it you should set it to ```True```.<br/>
```OE_PORT``` is the port where Odoo should run on, for example 8069.<br/>
```OE_VERSION``` is the Odoo version to install, for example ```14.0``` for Odoo V14.<br/>
```IS_ENTERPRISE``` will install the Enterprise version on top of ```14.0``` if you set it to ```True```, set it to ```False``` if you want the community version of Odoo 14.<br/>
```OE_SUPERADMIN``` is the master password for this Odoo installation.<br/>
```INSTALL_NGINX``` is set to ```False``` by default. Set this to ```True``` if you want to install Nginx.<br/>
```WEBSITE_NAME``` Set the website name here for nginx configuration<br/>
```ENABLE_SSL``` Set this to ```True``` to install [certbot](https://github.com/certbot/certbot) and configure nginx with https using a free Let's Encrypted certificate<br/>
```ADMIN_EMAIL``` Email is needed to register for Let's Encrypt registration. Replace the default placeholder with an email of your organisation.<br/>
```INSTALL_NGINX``` and ```ENABLE_SSL``` must be set to ```True``` and the placeholder in ```ADMIN_EMAIL``` must be replaced with a valid email address for certbot installation<br/>
  _By enabling SSL though Let's Encrypt you agree to the following [policies](https://www.eff.org/code/privacy/policy)_ <br/>

#### 5. Make the script executable
```
sudo chmod +x odoo_install.sh
```
##### 6. Execute the script:
```
sudo ./odoo_install.sh
```


