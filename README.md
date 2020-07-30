# Docker-Wordpress

Aim:- Project is capable to setup the wordpress web app in just one click by getting all the infrastructure ready in just one go.

Technology used:- Docker on the host OS (Redhat Linux 8)

About Project :-This project is based on Docker and with the help of certain methods like(patting for outside accessibility , volume usage for permanent storage of data and docker compose) , this project can be created.

Docker compose:- Docker compose enables "Infrastructure as code" , By creating ".yml / .yaml" file you can first code and save all your commands in that file.Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application's services. ... Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment.

 WordPress is the simplest, most popular way to create your own website or blog.

Implementing wordpress on docker and establishing connection with mysql. There are following important concepts, which is required before developing this project-->

*Docker requires ISO/image file for installation of containers(OS)
For the downloading the ISO/image files you can go to download it from docker-hub or by using following command download the images first

	mysql image:-	        docker pull mysql:5.7
	nextcloud image :-	docker pull nextcloud:latest

*Now there is the dependency of wordpress on database server(here we have take- mysql) so launch "mysql" container(named - dbos) first then launch "wordpress" container.

*Written code in .yml file so that our code is safe either the container gets removed hence promoting "Infrastructure as cloud" so in the same repository there is "docker-compose.yml" file having the main code written.

*We have used "volume concept" for storing the data permanently 

*Patting concept :- PAT (Port Address Translation) so that our container will have outside connectivity.

*For running docker-compose.yml file:-
	docker-compose up -d
*For stopping containers:-
	docker-compose stop
*For again starting docker containers:-
	docker-compose start
