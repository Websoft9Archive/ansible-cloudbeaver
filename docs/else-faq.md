# FAQ

#### 本项目中 CloudBeaver 采用何种安装方式？

Docker

#### CloudBeaver 采用何种驱动连接数据库？

JDBC 驱动


#### Can I reset password of CloudBeaver by command?

不可以，只支持控制台修改

#### CloudBeaver 是否支持创建数据库？

暂未发现此功能

#### 如何更改 CloudBeaver 的默认方式方式

修改 [Nginx虚拟机主机配置文件](/zh/stack-components.md#nginx)，将其中的 **server_name** 项的 `listen 80` 修改成类似 `listen 8090` 即可

#### If there is no domain name, can I deploy CloudBeaver?

Yes, access CloudBeaver by *http://Server's Internet IP*.

#### What is the password for the database root user?

The password is stored in the server related file `/credentials/password.txt`.

#### Is it possible to modify the source path of CloudBeaver?

No.

#### How to change the permissions of filesystem?

Change owner(group) or permissions as below:

```shell
chown -R nginx.nginx /data/wwwroot
find /data/wwwroot -type d -exec chmod 750 {} \;
find /data/wwwroot -type f -exec chmod 640 {} \;
```

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a series of software to the server in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference. All refer to cloud servers. They are the different terminology used by manufacturers.
