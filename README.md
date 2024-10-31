#install and check
~~~~
sudo apt update
sudo apt install openjdk-17-jre
java -version
~~~~

#install jenkins in ubuntu
~~~~
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
~~~~
#Open port 8080 in the inbound traffic rules
~~~~
instances > security > security group
add a rule for port 8080
~~~~
~~~~
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
~~~~
#install docker 
~~~~
sudo apt update
sudo apt install docker.io

sudo su - 
usermod -aG docker jenkins
usermod -aG docker ubuntu
systemctl restart docker

RESTART
~~~~
