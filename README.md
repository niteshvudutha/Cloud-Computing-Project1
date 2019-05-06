INSTALLING DOCKER ON UBUNTU:

INSTALL DOCKER CE: 

    Install packages to allow apt to use a repository over HTTPS:
        sudo apt-get install \
        apt-transport-https \
        ca-certificates \
        curl \
        gnupg-agent \
        software-properties-common
    Add Docker’s official GPG key:
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    Verifying key with fingerprint
        sudo apt-key fingerprint 0EBFCD88
    To set up the stable repository:
            sudo add-apt-repository \
            "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
            $(lsb_release -cs) \
            stable"
    Install the latest version of Docker CE and containerd:
        sudo apt-get install docker-ce docker-ce-cli containerd.io
    Start the Docker service:
        sudo service docker start
    Add ubuntu to the docker group to execute Docker commands without using sudo:
        sudo usermod -a -G docker ec2-user
    Log out and log back in again to pick up the new docker group permissions
    Login to docker with the Docker Hub Account:
    docker login -u username
    password

BUILDING DOCKER IMAGE:

    Create a folder:
        sudo mkdir /var/ccpro1

    To transfer files using WinSCP:    
        sudo chown -R ubuntu:ubuntu /var/ccpro1

    Transfer the project files along with the dockerfile into 'ccpro1' folder
    Get to the below location:
        cd /var/ccpro1/

    To build a image present in the current location with a image name and version:
        docker build -t appyimage:1.0 .

    Run the image by specifying it's image number(use: docker images):
        docker run -p 80:80 <image-number>

    Commit the container with it's container numer(use: docker ps):
        docker commit 8e3eea53b673 ayyappadoc/8e3eea53b673
    
    Push the image into dockerhub:
        docker push ayyappadoc/8e3eea53b673

USING THE BUILT DOCKER IMAGE:

        docker pull ayyappadoc/8e3eea53b673

        docker run -p 80:80 ayyappadoc/8e3eea53b673
# Cloud-Computing-Project1
