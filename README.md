# influxdbgrafanaansible

Only tested with ansible 2.2 and 2.4

# How to use directly on raspberry pi# 
Make sure you have ansible installed on you raspberry pi

`sudo apt-get install ansible`

Then run ansible-playbook 

`ansible-playbook play.yml --c local -i "localhost," --ask-become-pass`

# How to run from different linux machine#
Make sure you have ansible installed.

ubuntu:

`sudo apt-get install ansible`

fedora:

`sudo dnf install ansible`

Then make sure you ssh public key is registered as an authorized key on the raspberry pi so ansible can login to the raspberry pi.

`ssh-copy-id [username]@[ip address]`

Then try and login on the raspberry pi via ssh and ensure you get no password prompt.

`ssh [username]@[ip address]`

Then you can run the ansible playbook from your machine.

`ansible-playbook play.yml -i "[ip address]," -u [username] --ask-become-pass`

For example:

`ansible-playbook play.yml -i "192.168.0.4," -u pi --ask-become-pass`
