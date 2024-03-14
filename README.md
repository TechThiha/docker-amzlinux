# docker-amzlinux

**Installing Docker on Amazonlinux**

sudo yum install docker

sudo service docker start

sudo usermod -a -G docker ec2-user

**Make sure to auto-start the Docker**

sudo chkconfig docker on

**Then install the git for installing docker compose**

sudo yum install -y git

**Then reboot the system.**

sudo reboot

**(or)**

We can use "sudo systemctl start docker" to start docker immediately. As we have installed the docker, we still need to install docker-compose.

**Let's install docker-compose**
Copy the appropriate docker-compose binary from GitHub:

sudo curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose

**NOTE: To get the latest version (thanks @spodnet): sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose**

Fix permissions after download:

sudo chmod +x /usr/local/bin/docker-compose

**Use this command to make sure the docker-compose is running.**
docker-compose version

You've successfully installed the docker on amazon linux!
