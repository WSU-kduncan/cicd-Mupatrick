Part 1 - Dockerize it

Milestone Participation due 11/19

Documentation

Create README.md in main folder of your repo that details the following:
-	vim README.md

Project Overview

Run Project Locally

how you installed docker + dependencies (WSL2, for example)

install docker with ubuntu (no need for WSL2 I am using Mac)
-	sudo apt  install docker.io
-	sudo snap install docker
-	docker --version (for version check)

how to build the container

docker build -t image_name:tag_version (example: docker build -t web:latest)

how to run the container

-	docker run -dit -p port:80 image_name:tag_version(example docker run -dit -p 8080:80 web:latest)

how to view the project (open a browser...go to ip and port...)
docker ps -a


Part 2 - GitHub Actions and DockerHub

Milestone Participation due 12/3

Documentation

Update README.md in main folder of your repo to include:

Create DockerHub public repo

  process to create

- After sign in or  create account if you don’t have one by using this link https://hub.docker.com/ 
- Click on create repository 
- Fill out the docker detail “name and description if you want to) 
- Under visibility select public then click create

  Prove

![docker hub](https://user-images.githubusercontent.com/77375881/144696354-86986300-3697-4abd-a63a-bb5d04c434e0.jpeg)


Allow DockerHub authentication via CLI using Dockhub credentials

- Log in to hub.docker.com.
- Click on your username in the top right corner and select Account Settings.
- Select Security > New Access Token.
- Add a description for your token. 
- Then set up the access permission from drop down 

   Prove


![Q Search by repository name](https://user-images.githubusercontent.com/77375881/144696435-e6a81a3e-aa36-4bbb-a58f-67cefe2b30cb.jpeg)




Configure GitHub Secrets

what credentials are needed - DockerHub credentials (do not state your credentials)


- Username
- Password or token as alternative

set secrets and secret names

Create .github folder
Create workflows folder inside .github and set the secrete in 
or
Go on GitHub.com
Navigate to the main page of the repository. 
under the repository name, click Actions. 
If you already have a workflow in your repository 
click New workflow and use the template that you want to use, 
then click start commit 

Configure GitHub Workflow
variables to change (repository, etc.)

- Navigate to the workflow
- Click Review deployments
- Select the job environment(s) to approve or reject. Optionally, leave a comment
- Approve or reject
- To approve the job, click Approve and deploy
- To reject the job, click Reject. If a job is rejected, the workflow will fail.


Part 3 - Deployment

Pulling the image
sudo docker pull mupatrick/myfirstdocker:latest

![RllebServ1 $ sudo docker pull mupatrickmyfirsdockerlat](https://user-images.githubusercontent.com/77375881/145256079-5a09ecea-50d6-4305-9de1-2e6caa1c6e70.jpeg)

Running the container
sudo docker run -dit -p 8080:80 mupatrick/myfirstdocker

![homeubuntu](https://user-images.githubusercontent.com/77375881/145256140-45fc04f2-3503-45db-b14e-a0810fcd02bc.jpeg)


![sudo docker ps](https://user-images.githubusercontent.com/77375881/145256160-88ba9527-885c-4b16-85bb-f68aaf50ac3c.jpeg)


