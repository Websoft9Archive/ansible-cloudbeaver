# Initial Installation

If you have completed the CloudBeaver deployment, follow the steps below to start a quick use.

## Preparation

1. Get the **Server's Internet IP** of Server on your Cloud Platform.
2. Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:80** is allowed.
3. Make a domain resolution on your Cloud Console if you want to use domain for CloudBeaver.

## CloudBeaver Installation Wizard

1. Use local browser to access the URL *http://Server's Internet IP*. enter to CloudBeaver wizard
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard001-websoft9.png)

2. Set your username and password, then click 【Next】 button
   ![init CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard002-websoft9.png)

3. Continue click【Next】 and click 【FINISH】 to complete it
   ![init CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard003-websoft9.png)

4. You can see a SQlite demo connection now
   ![init CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard004-websoft9.png)

5. Go to: 【Administrator】>【Connection Management】, delete【SQLite - Chinook (Sample)】 to avoid security trouble
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard005-websoft9.png)

6. Go to home page, you can't see the SQLite demo now

> More guide about CloudBeaver, please refer to [CloudBeaver Documentation](https://cloudbeaver.io/docs/).

## CloudBeaver Setup wizard

Coming soon...

## Q&A

#### Can't visit the start page of CloudBeaver?

Your TCP:80 of Security Group Rules is not allowed, so there is no response from Chrome or Firefox.

#### Can I access CloudBeaver by other port?
 
9090, this deployment solution use Nginx proxy from 9090 to 80
