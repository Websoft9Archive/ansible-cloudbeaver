---
sidebarDepth: 3
---

# Parameters

The CloudBeaver deployment package contains a sequence of software (referred to as "components") required for CloudBeaver to run. Below list the important information, the component name, installation directory path, configuration file path, port, version, etc.

## Path

This solution use Docker to deploy all service, you can run the command `docker ps` to list them  

```
CONTAINER ID   IMAGE                        COMMAND             CREATED       STATUS       PORTS                                       NAMES
34baab38d75f   dbeaver/cloudbeaver:latest   "./run-server.sh"   3 hours ago   Up 3 hours   0.0.0.0:8080->8978/tcp, :::8080->8978/tcp   cloudbeaver
```

### CloudBeaver

CloudBeaver root directory: */data/apps/cloudbeaver*  
CloudBeaver volumes: */data/apps/cloudbeaver/volumes*  
CloudBeaver configuration file: */data/apps/cloudbeaver/volumes/GlobalConfiguration/.dbeaver/data-sources.json*  

> data-sources.json storage the database connection files

### Nginx

Nginx vhost configuration file: */etc/nginx/conf.d/default.conf*    
Nginx main configuration file: */etc/nginx/nginx.conf*   
Nginx logs file: */var/log/nginx*  
Nginx rewrite rules directory: */etc/nginx/conf.d/rewrite*  
Nginx htpasswd file: */etc/nginx/.htpasswd/htpasswd.conf*  

### Docker

Docker root directory: */var/lib/docker*  
Docker image directory: */var/lib/docker/image*   
Docker daemon.json: please create it when you need and save to to the directory */etc/docker*   

## Ports

Open or close ports by **[Security Group Setting](https://support.websoft9.com/docs/faq/tech-instance.html)** of your Cloud Server to decide whether the port can be accessed from Internet.  

You can run the cmd `netstat -tunlp` to check all related ports.  

The following are the ports you may use:

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| TCP | 80 | HTTP to access CloudBeaver | Required |
| TCP | 443 | HTTPS to access CloudBeaver | Optional |
| TCP | 9090 | HTTP to access CloudBeaver | Optional |

## Version

You can see the version on product pages at Marketplace. However, after being deployed to your server, the components will be updated automatically, resulting in a certain change in the version number. Therefore, run the command on the server to view the exact version number. 

```shell
# Check all components version
sudo cat /data/logs/install_version.txt

# Linux Version
lsb_release -a

# Nginx  Version
nginx -V

# Docker Version
docker -v

# CloudBeaver version

```
