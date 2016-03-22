# A linux_server
i. IP address: 52.24.239.208; SSH port: 2200

ii. The complete URL to my hosted web application:
http://ec2-52-24-239-208.us-west-2.compute.amazonaws.com/

iii. softwares installed and configuration changes made:
  - to upgrade packages of the Ubuntu environment:
    - sudo apt-get update
    - sudo apt-get dist-upgrade
  - to establish virtual machine at the remote server at /var/www/FoodTherapy/FoodsTherapy:
    - sudo pip install virtualenv
    - sudo virutalenv venv
    - source venv/bin/activate
  - inside the venv, install the following to serve the app:
    - pip install flask
    - pip install httplib2
    - pip install requests
    - pip install oauth2client
    - pip install imgurpython
    - pip install sqlalchemy
  - set up a user and its password, and establish its ssh using public key/private key pair
    authentication
  - edit 'Authorized redirect URIs' of app credentials at google API Manager tab
  - register app at 'facebook for developers' and provide 'Valid OAuth redirect
    URIs' and 'Site URL' at the app's Settings tab
  - set up and enable firewall including denying access via port 22
  - in /etc/ssh/sshd_config, disable password login and root login, reset port.
  - install Glances
    - sudo apt-get install python-pip build-essential python-dev
    - sudo pip install Glances
    - sudo apt-get install lm-sensors
    - sudo pip install pysensors
  - install Fail2Ban

iv. third-party resources, including:
  - https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
  - https://github.com/carwin/markdown-styleguide
  - https://developers.facebook.com/
  - https://console.developers.google.com
  - https://api.imgur.com/
  - http://stackoverflow.com/
  - http://askubuntu.com/questions/293426/system-monitoring-tools-for-ubuntu
  - https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-fail2ban-on-
    ubuntu-14-04
