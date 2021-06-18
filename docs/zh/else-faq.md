# FAQ

#### CloudBeaver 是否支持多语言？

支持（包含中文）后台直接切换语言，但目前中文语言包不完整

#### CloudBeaver 支持哪些数据库？

默认支持 

#### 本项目中 CloudBeaver 采用何种安装方式？

Docker

#### CloudBeaver 采用何种驱动连接数据库？

JDBC 驱动


#### 是否可以通过命令行修改CloudBeaver后台密码？

不可以，只支持控制台修改

#### CloudBeaver 是否支持创建数据库？

暂未发现此功能

#### 如果没有域名是否可以部署 CloudBeaver？

可以，访问`http://服务器公网IP` 即可

#### 如何更改 CloudBeaver 的默认访问方式？

修改 [Nginx虚拟机主机文件](/zh/stack-components.md#nginx)，将其中的 **server_name** 项 `listen 80` 修改成类似 `listen 8090` 即可

#### 数据库 root 用户对应的密码是多少？

密码存放在服务器相关文件中：`/credentials/password.txt`

#### 是否有可视化的数据库管理工具？

有，内置phpMyAdmin，访问地址：*http://服务器公网IP:9090*

#### 如何禁止外界访问phpMyAdmin？

连接服务器，编辑 [phpMyAdmin 配置文件](/zh/stack-components.md#phpmyadmin)，将其中的 `Require all granted` 更改为 `Require ip 192.160.1.0`，然后重启 Apache 服务

#### 是否可以修改CloudBeaver的源码路径？

不可以

#### 如何修改上传的文件权限?

```shell
# 拥有者
chown -R nginx.nginx /data/wwwroot/
# 读写执行权限
find /data/wwwroot/ -type d -exec chmod 750 {} \;
find /data/wwwroot/ -type f -exec chmod 640 {} \;
```

#### 部署和安装有什么区别？

部署是将一序列软件按照不同顺序，先后安装并配置到服务器的过程，是一个复杂的系统工程。  
安装是将单一的软件拷贝到服务器之后，启动安装向导完成初始化配置的过程。  
安装相对于部署来说更简单一些。 

#### 云平台是什么意思？

云平台指提供云计算服务的平台厂家，例如：Azure,AWS,阿里云,华为云,腾讯云等

#### 实例，云服务器，虚拟机，ECS，EC2，CVM，VM有什么区别？

没有区别，只是不同厂家所采用的专业术语，实际上都是云服务器
