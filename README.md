# test-traefik

### To deploy in swarm
`sudo docker network create --scope swarm web`

`sudo docker volume create --name=wordpress`

`sudo docker stack deploy -c traefik.yaml stack-traefik`

`sudo docker stack deploy -c wordpress.yaml stack-wordpress`
