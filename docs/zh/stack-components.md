---
sidebarDepth: 3
---

# 参数

CloudBeaver 预装包包含 CloudBeaver 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

本部署方案中的 CloudBeaver 采用 Docker 部署，运行 `docker ps` 查看运行的容器。
```
CONTAINER ID   IMAGE                        COMMAND             CREATED       STATUS       PORTS                                       NAMES
34baab38d75f   dbeaver/cloudbeaver:latest   "./run-server.sh"   3 hours ago   Up 3 hours   0.0.0.0:8080->8978/tcp, :::8080->8978/tcp   cloudbeaver
```

### CloudBeaver

CloudBeaver 安装目录： */data/apps/cloudbeaver*  
CloudBeaver 存储目录： */data/apps/cloudbeaver/volumes*  
CloudBeaver 配置文件： */data/apps/cloudbeaver/volumes/GlobalConfiguration/.dbeaver/data-sources.json*  

> data-sources.json 存放数据库连接信息

### Nginx

Nginx 虚拟主机配置文件：*/etc/nginx/conf.d/default.conf*  
Nginx 主配置文件： */etc/nginx/nginx.conf*  
Nginx 日志文件： */var/log/nginx*  
Nginx 伪静态规则目录： */etc/nginx/conf.d/rewrite*  
Nginx 验证访问文件：*/etc/nginx/.htpasswd/htpasswd.conf*  

### Docker

Docker 根目录: */var/lib/docker*  
Docker 镜像目录: */var/lib/docker/image*   
Docker daemon.json 文件：默认没有创建，请到 */etc/docker* 目录下根据需要自行创建   

### Redis

Redis 配置文件： */etc/redis.conf*  
Redis 数据目录： */var/lib/redis*  
Redis 日志文件： */var/log/redis/redis.log*

## 端口号

在云服务器中，通过 **[安全组设置](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** 来控制（开启或关闭）端口是否可以被外部访问。 

通过命令`netstat -tunlp` 看查看相关端口，下面列出可能要用到的端口：

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| TCP | 80 | 通过 HTTP 访问 CloudBeaver 控制台 | 可选 |
| TCP | 443 | 通过 HTTPS 访问 CloudBeaver 控制台 | 可选 |
| TCP | 9090 | 通过 HTTP 访问 CloudBeaver 控制台 | 可选 |

## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

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
