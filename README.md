# registry-lab

## Reference

    https://docs.docker.com/registry/deploying/

## Create user/password

    htpasswd -Bbn [user] [password] > auth/htpasswd

## Run Registry
    
    docker-compose up -d

## On client side (unsecure)

    vi /etc/docker/daemon.json

Add the following:

    {
    "insecure-registries":["<Server IP>:5000"]
    }

Example:

    {
    "insecure-registries":["192.168.8.113:5000"]
    }