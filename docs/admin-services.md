# Start or Stop the Services

These commands are required when you use the CloudBeaver of Websoft9.

### CloudBeaver

```shell
sudo docker start cloudbeaver
sudo docker stop cloudbeaver
sudo docker restart cloudbeaver
sudo docker stats cloudbeaver
```

### Docker

```shell
sudo systemctl start docker
sudo systemctl restart docker
sudo systemctl stop docker
sudo systemctl status docker
```

### Docker-compose

```
# Create containers
sudo docker-compose up

# Create containers at backend
sudo docker-compose up -d

# Restart/Stop/Start
sudo docker-compose start
sudo docker-compose stop
sudo docker-compose restart
```

### Nginx

```shell
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```