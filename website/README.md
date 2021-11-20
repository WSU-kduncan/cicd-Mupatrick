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

