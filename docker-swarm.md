Docker swarm is container orchestration tools.
  - 	Helps deploy containers across multiple server/vms/cluster
	-   Provides desired state
	-   Scale up and down across the servers/vm/cluster
  

Basic commands:

## which ever vm we will run this command, will act as a master/manager vm ##
docker swarm init

## To join worker node to a master node ###
docker swarm join

## TWO TYPES OF SERVICES IN DOCKER SWARM 
Replicated mode and global mode

<img src="https://github.com/seemathapliyal79/docker/blob/main/screenshots/docker-swarm-types-of-services.png">
