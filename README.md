# A linux_server
i. IP address: 52.24.239.208; SSH port: 2200

ii. The complete URL to my web application hosted at Amazon Web Services platform:
http://ec2-52-24-239-208.us-west-2.compute.amazonaws.com/

iii. softwares installed and configuration changes made:
  - set up a user and its password, and establish its ssh using public key/private key
    pair authentication
  - edit 'Authorized redirect URIs' of app credentials at google API Manager tab
  - register app at 'facebook for developers' and provide 'Valid OAuth redirect
    URIs' and 'Site URL' at the app's Settings tab
  - set up and enable firewall including denying access via port 22
  - in /etc/ssh/sshd_config, disable password login and root login, reset port.
  
  --------(As the new user)--------
  - upgrade packages of the Ubuntu environment:
    - sudo apt-get update
    - sudo apt-get dist-upgrade
  - to establish virtual machine at the server at /var/www/FoodTherapy/FoodsTherapy:
    - sudo pip install virtualenv
    - sudo virutalenv venv
    - source venv/bin/activate
  - inside the venv, install the following to serve the app:
    - sudo pip install flask
    - sudo pip install httplib2
    - sudo pip install requests
    - sudo pip install oauth2client
    - sudo pip install imgurpython
    - sudo pip install sqlalchemy
  
  - to monitor the linux system install Glances per resource #7.
    - sudo apt-get install python-pip build-essential python-dev
    - sudo pip install Glances
    - sudo apt-get install lm-sensors
    - sudo pip install pysensors
  - install Fail2Ban, enabling jail nginx-http-auth and jail ssh per resource #8.
  - set up automatic updates, by the following per resource #9
    - sudo apt-get install unattended-upgrades
    - edit /etc/apt/apt.conf.d/50unattended-upgrades
    - edit /etc/apt/apt.conf.d/10periodic

iv. third-party resources, including:
  1. https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-
     ubuntu-vps
  2. https://github.com/carwin/markdown-styleguide
  3. https://developers.facebook.com/
  4. https://console.developers.google.com
  5. https://api.imgur.com/
  6. http://stackoverflow.com/
  7. http://askubuntu.com/questions/293426/system-monitoring-tools-for-ubuntu
  8. https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-fail2ban-
     on-ubuntu-14-04
  9. https://help.ubuntu.com/lts/serverguide/automatic-updates.html
