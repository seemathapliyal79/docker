Docker swarm is container orchestration tools.
  - 	Helps deploy containers across multiple server/vms/cluster
	-   Provides desired state
	-   Scale up and down across the servers/vm/cluster
  

Basic commands:

## which ever vm we will run this command, will act as a master/manager vm ##
docker swarm init

## To Create a token for worker node to join the swarm cluster.. This command is run on master node ###
docker swarm join-token worker

## Some related commands of swarm cluster
''Demote one or more nodes from manager in the swarm ''
docker node demote						
docker node inspect						## Display detailed information on one or more nodes ##
docker node ls							## List nodes in the swarm
docker node promote						## Promote one or more nodes to manager in the swarm
docker node ps							## List tasks running on one or more nodes, defaults to current node
docker node rm							## Remove one or more nodes from the swarm
docker node update						## Update a node
docker info | grep -i swarm					## on worker node to check the swarm status

## TWO TYPES OF SERVICES IN DOCKER SWARM 
Replicated mode and global mode

<img src="https://github.com/seemathapliyal79/docker/blob/main/screenshots/docker-swarm-types-of-services.png">




docker service create --name myapp --mode replicated --replicas 7 -p 9080:3000 lerndevops/samples:pyapp-v1
docker service create --name mydb --mode replicated --replicas 3 -p 9081:27017 mongo:latest
