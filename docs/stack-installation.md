# Initial Installation

If you have completed the RabbitMQ deployment, follow the steps below to start a quick use.

## Preparation

1. Get the **Server's Internet IP** of Server on your Cloud Platform.
2. Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:8161** is allowed.
3. Make a domain resolution on your Cloud Console if you want to use domain for RabbitMQ.

## RabbitMQ Installation Wizard

1. Use local Chrome or Firefox to access the URL *http://DNS:15672* or *http://Server's Server's Internet IP:15672*. You will enter installation wizard of RabbitMQ.
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/rabbitmq/rabbitmq-login-websoft9.png)

2. Log in RabbitMQ web console. ([Don't have password?](/stack-accounts.md#rabbitmq)) 
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/rabbitmq/rabbitmq-bk-websoft9.png)

3. Set you new password from: 【Users】>【Admin】>【Permissions】>【Update this user】
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/rabbitmq/rabbitmq-pw-websoft9.png)

> More guide about RabbitMQ, please refer to [RabbitMQ Documentation](https://www.rabbitmq.com/documentation.html).

## RabbitMQ Setup wizard

## Q&A

#### Can't visit the start page of RabbitMQ?

Your TCP:15672 of Security Group Rules is not allowed, so there is no response from Chrome or Firefox.

#### RabbitMQ service can't start? 
Reason:  
Solution:  
