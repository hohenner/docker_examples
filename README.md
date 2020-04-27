# environments
sample virtualized environments for experimentation and learning 

# install Docker
## Ubuntu
https://docs.docker.com/engine/install/ubuntu/

1. Uninstall old versions:
    1. `sudo apt-get remove docker docker-engine docker.io containerd runc`
2. update apt-get:
    1. `sudo apt-get update`
3. install dependancies:
    1. `sudo apt-get install apt-transport-https  ca-certificates curl gnupg-agent software-properties-common`
4. add docker's GPG key:
    1. `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
    2. validate GPG key:
        1. `sudo apt-key fingerprint 0EBFCD88`
        2. should be `9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88`
5. setup docker repository:
    1. `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`
6. install Docker engine
    1. update apt-get again: `sudo apt-get update`
    2. `sudo apt-get install docker-ce docker-ce-cli containerd.io`
7. Validate that docker was installed correctly
    1. `sudo docker run hello-world`