## Project 1: Docker and Web Services ##

## NITESH VUDUTHA #M12483636

## Submission Date : 05-06-2019

This project is a dockerised image for the Homework3.
The code is available here https://github.com/niteshvudutha/Cloud-Computing-HW3.git

#Environement Setup

1. Install packages that will allow the github repository to be used in HTTPS connection

2. Then add the Docker's official key 
   "curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -"
   
3. Now, verify key and set up stable repository using the commands
   "sudo apt-key fingerprint 0EBFCD88"
   "sudo add-apt-repository \"

4. Install or Update the Docker to its latest version

5. Start Docker by command
   "sudo service docker start"
   "sudo usermod -a -G docker ec2-user" (ec2-user for Amazon instance users)
   
6. Authorize docker with docker hub account


#Downloading and coping the Weather application Docker image

1. The docker image is with .tgz format.
   The file is uploaded in the google drive because github cannot host such a large file.
   Download the file from the below link: https://drive.google.com/open?id=1awRrM0PxCNl7E62AN7sboXmujqYeEcGo
   
2. Using WinSCP or similar app copy the file into aws EC2 instance
 

#Executing the above Docker image

1. Follow the below command to load docker file
   
   docker load -i final_project.tar

2. Now execute the docker image using 

   docker run -p 80:80 nitesh:1.0

3. Verify the application in the browser

4. Expected Output screenshot is in below link

   https://drive.google.com/file/d/1yPMV8aFSDxQV9IPx0MxYHVCe-0S8ZGtR/view?usp=sharing









