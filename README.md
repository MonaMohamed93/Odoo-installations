# Odoo-installations
Odoo Enterprise and community run for ubuntu


In this tutorial I will learn you how to install Odoo 12 community or enterprise on Ubuntu 18.04. The script that you will use is based on the code from André Schenkels but has been updated, upgraded and improved. Do notice that if you want to install the enterprise version that you will need to be an official partner or that you need to have bought the enterprise subscription from Odoo. Otherwise you will have no access to the Github repository for the enterprise code!
1. Downloading the script

The first step is to download my script from Github and to add the code in a new .sh file on your Ubuntu machine, wherever you’d like this.
For example right under /home. Open up an Ubuntu terminal and cd to the directory where you’d like to keep the script and then create the file:
sudo wget https://raw.githubusercontent.com/Yenthe666/InstallScript/12.0/odoo_install.sh


If you’re curious about how the whole code looks and works you can find it on my Github account.
Now open up the file and edit the parameters to your liking:
sudo nano odoo_install.sh


There are some things you can configure/change to your likings at the top of the script. You can choose if you wish to install Wkhtmltopdf or not, which version you’d like, where the location is and most importantly what the master admin password is.
Tip: always modify this for every Odoo you install!
If you want the enterprise version of V12 you should change the line IS_ENTERPRISE to true:
IS_ENTERPRISE="True"


If you want the community version you can just continue and keep the IS_ENTERPRISE key on “False” (which is the case by default):
IS_ENTERPRISE="False"


2. Making the Odoo installation file executable

The next step is to make this file executable. After you’ve made it executable you can execute it and everything will be installed automatically.
do this with the following command:
sudo chmod +x odoo_install.sh


3.Running the script

Now that the code is in your file and the file is executable you simply have to execute it with the following command:
./odoo_install.sh


You will see that the script automatically starts updates, downloads required packages, creates the user, downloads the code from Github, … Eventually, if you’ve chosen to install the enterprise version, you will need to give in your Github credentials to download the enterprise code (since this is a private repository). Fill in your details and let the script continue:


Odoo 12 enterprise authentication
Give the script a few minutes to configure and install everything and eventually you will see something like this:
"
Done! The Odoo server is up and running. Specifications:
Port: 8069
User service: odoo
User PostgreSQL: odoo
Code location: odoo
Addons folder: odoo/odoo-server/addons/
Start Odoo service: sudo service odoo-server start
Stop Odoo service: sudo service odoo-server stop
Restart Odoo service: sudo service odoo-server restart  "

You now have a fully functional Odoo V12 community or enterprise on your system! Congratulations.
Odoo V12

