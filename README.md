# For setting up the browser server on an ec2 t3.medium machine with Amazon Linux 2 AMI

1) in Route 53, create a record set for the chosen domain name that points to the machine's IP address
2) ssh to the machine as ec2-user
3) sudo yum update
4) wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
5) sudo yum install epel-release-latest-7.noarch.rpm 
6) sudo yum install emacs
7) sudo yum install python2-pip
8) ssh-keygen -t rsa -b 4096
9) eval $(ssh-agent -s)
10) ssh-add ~/.ssh/id_rsa
11) add the public key  ~/.ssh/id_rsa.pub to your github account
12) wget https://dl.eff.org/certbot-auto
13) sudo mv certbot-auto /usr/local/bin/certbot-auto
14) sudo chown root /usr/local/bin/certbot-auto
15) sudo chmod 0755 /usr/local/bin/certbot-auto
16) in /usr/local/bin/certbot-auto, replace the line `elif [ -f /etc/issue ] && grep -iq "Amazon Linux" /etc/issue ; then` with `elif grep -i "Amazon Linux" /etc/issue > /dev/null 2>&1 || grep 'cpe:.*:amazon_linux:2' /etc/os-release > /dev/null 2>&1; then`
17) sudo /usr/local/bin/certbot-auto certonly --standalone --debug 
18) sudo yum install git
19) sudo yum install mysql
20) sudo yum install mysql-devel
21) sudo pip install cherrypy
22) sudo pip install MySQL-python

# For setting up the android server an ec2 t3.medium machine with Amazon Linux 2 AMI
1) in Route 53, create a record set for the chosen domain name that points to the machine's IP address
2) ssh to the machine as ec2-user
3) sudo yum update
4) curl -sL https://rpm.nodesource.com/setup_14.x | sudo bash -
5) sudo yum install -y nodejs
6) sudo npm install mysql
7) sudo yum install mysql
8) sudo yum install mysql-devel
9) sudo yum install emacs
10) sudo yum install git
11) ssh-keygen -t rsa -b 4096
12) eval $(ssh-agent -s)
13) ssh-add ~/.ssh/id_rsa
14) add the public key  ~/.ssh/id_rsa.pub to your github account
15) wget https://dl.eff.org/certbot-auto
16) sudo mv certbot-auto /usr/local/bin/certbot-auto
17) sudo chown root /usr/local/bin/certbot-auto
18) sudo chmod 0755 /usr/local/bin/certbot-auto
19) in /usr/local/bin/certbot-auto, replace the line `elif [ -f /etc/issue ] && grep -iq "Amazon Linux" /etc/issue ; then` with `elif grep -i "Amazon Linux" /etc/issue > /dev/null 2>&1 || grep 'cpe:.*:amazon_linux:2' /etc/os-release > /dev/null 2>&1; then`
20) sudo /usr/local/bin/certbot-auto certonly --standalone --debug 
