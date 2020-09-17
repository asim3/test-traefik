# test-traefik

### To deploy in swarm
##### start swarm
`sudo docker swarm init --advertise-addr eth1`

##### add network and volume
`sudo docker network create --scope swarm web`

`sudo docker volume create --name=wordpress`


##### deploy
`sudo docker stack deploy -c traefik.yaml stack-traefik`

`sudo docker stack deploy -c wordpress.yaml stack-wordpress`
