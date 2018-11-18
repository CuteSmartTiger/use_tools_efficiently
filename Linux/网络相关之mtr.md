sudo apt-get -y install mtr


mtr -4 -n -p


mtr -4 -n -p 192.168.5.19 > /var/log/mtr.log
