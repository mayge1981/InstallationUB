# Installation

1. Install WSL and Ubuntu
   1. Open your windows terminal (command)
   2. wsl --intall
   3. wsl --install -d Ubuntu
   4. create username and password
   5. wsl
   * resources: https://learn.microsoft.com/en-us/windows/wsl/install

2. Install Docker inside of Ubuntu WSL
   1. sudo apt-get update
   2. sudo apt-get install ca-certificates curl gnupg lsb-release
   3. sudo mkdir -p /etc/apt/keyrings
   4. curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
   5. echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   6. sudo apt-get update
   7. sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
   8. sudo groupadd docker
   9. sudo usermod -aG docker $USER
   10. exit
   11. wsl --shutdown
   12. wsl
   13. sudo service docker start
   14. Try to download images
       1. docker pull tomcat:8.5.82-jdk8-corretto-al2
       2. docker pull centos:centos7.9.2009

   * Resources:
     * https://docs.docker.com/engine/install/ubuntu/
     *https://docs.docker.com/engine/install/linux-postinstall/


3. Docker demo repository
   1. https://github.com/mayge1981/SpringBootDockerUB.git
   2. https://github.com/mayge1981/SpringBootMysqlDockerUB.git
   3. https://github.com/mayge1981/haproxyDockerUB.git


4. Source codes
