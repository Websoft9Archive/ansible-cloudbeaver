# More

Each of the following solutions has been proved to be effective and we hope it can give you help.

## Binding Domain

The precondition for binding a domain is that CloudBeaver can accessed by domain name.

When there is only one website on the server, you can visit the website without binding domain. While considering the server security and subsequent maintenance, **Binding Domain** is necessary.

Steps for binding CloudBeaver domain are as follows:

1. Connect your Cloud Server;
2. Modify [Nginx vhost configuration file](/stack-components.md#nginx),and change the **server_name**'s value to your domain name.
   ```text
   server
   {
   listen 80;
   server_name www.example.com;  # change it into your domain name
   ...
   }
   ```
3. Restart Nginx service
   ```
   sudo systemctl restart nginx
   ```

## Resetting Password

There are two main measures to reset password.

### Changing password

Take the steps below:

1. log in the CloudBeaver backend, 右上角打开：【Administrator】>【User】，找到所需修改密码的账号对象
  ![CloudBeaver 修改密码](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-modifypw-websoft9.png)

2. 开始修改密码，点击【Save】后生效

### Forgot Password

Try to retrieve your password 只能通过重置 CloudBeaver 容器的方式找回：

1. 使用 SSH 工具连接  CloudBeaver 服务器

2. 依次运行下面的命令
   ```
   cd /data/apps/cloudbeaver
   docker-compose down -v
   docker-compose pull
   docker-compose up -d
   ```

## 驱动管理

参考官方文档[Driver managements](https://cloudbeaver.io/docs/Driver-managements/)

## 导出数据

![](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-exportdata-websoft9.png)
