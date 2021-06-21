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

1. Login to CloudBeaver, Go to【Administrator】>【User】 of top right menu and find your account
  ![CloudBeaver modify password](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-modifypw-websoft9.png)

2. Modify password and click 【Save】

### Forgot Password

Retrieve your password need to recreate container

1. Use **SSH** to connect CloudBeaver instance

2. Run the below commands
   ```
   cd /data/apps/cloudbeaver
   docker-compose down -v
   docker-compose pull
   docker-compose up -d
   ```

## Drivers

Refer to [Driver managements](https://cloudbeaver.io/docs/Driver-managements/)

## Export data

![](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-exportdata-websoft9.png)
