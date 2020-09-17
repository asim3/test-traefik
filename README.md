# test-traefik


## Prerequisite
##### start swarm
`sudo docker swarm init --advertise-addr eth1`


##### add network and volume
`sudo docker network create --scope swarm web`

`sudo docker volume create --name=wordpress`


## To deploy in swarm
`sudo docker stack deploy -c traefik.yaml stack-traefik`

`sudo docker stack deploy -c wordpress.yaml stack-wordpress`    
`sudo docker stack deploy -c wordpress-2.yaml stack-wordpress-2`


## Monitoring
`sudo docker stack ps stack-traefik`

`sudo docker stack ps stack-wordpress`
