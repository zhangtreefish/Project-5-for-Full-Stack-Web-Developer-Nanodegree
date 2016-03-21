# A linux_server
i. IP address: 52.24.239.208; SSH port: 2200

ii. The complete URL to my hosted web application:
http://ec2-52-24-239-208.us-west-2.compute.amazonaws.com/

iii. softwares installed and configuration changes made:
  - to establish virtual machine at the remote server:
    - sudo pip install virtualenv
    - sudo virutalenv venv
    - source venv.bin/activate
  - inside the venv, install the following to serve the app:
    - pip install flask
    - pip install httplib2
    - pip install requests
    - pip install oauth2client
    - pip install imgurpython
    - pip install sqlalchemy
  - set up a user, and establish ssh using public key/private key pair
    authentication
  - edit 'Authorized redirect URIs' of app credentials at google API Manager tab
  - register app at 'facebook for developers' and provide 'Valid OAuth redirect
    URIs' and 'Site URL' at the app's Settings tab
  - set up and enable firewall including denying access via port 22
  - in /etc/ssh/sshd_config, disable password login and root login, reset port.

iv. third-party resources, including:
  - https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
  - https://github.com/carwin/markdown-styleguide
  - https://developers.facebook.com/
  - https://console.developers.google.com
  - https://api.imgur.com/
  - http://stackoverflow.com/
