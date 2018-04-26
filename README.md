# influxdbgrafanaansible

Only tested with ansible 2.3

# How to use directly on raspberry pi# 
Make sure you have ansible installed on you raspberry pi
`sudo apt-get install ansible`

Then run ansible-playbook 
`ansible-playbook play.yml --connection=local --ask-become-pass`
