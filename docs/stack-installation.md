# Initial Installation

If you have completed the CloudBeaver deployment, follow the steps below to start a quick use.

## Preparation

1. Get the **Server's Internet IP** of Server on your Cloud Platform.
2. Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:80** is allowed.
3. Make a domain resolution on your Cloud Console if you want to use domain for CloudBeaver.

## CloudBeaver Installation Wizard

1. Use local browser to access the URL *http://DNS* or *http://Server's Internet IP*. You will enter installation wizard of CloudBeaver.
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard001-websoft9.png)

2. 设置用户名和密码，然后点击【Next】进入下一步
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard002-websoft9.png)

3. 继续点击【Next】进入下一步，最后点击【FINISH】完成初始化
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard003-websoft9.png)

4. 默认已经存在一个 SQlite 的演示连接
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard004-websoft9.png)

5. 通过：【Administrator】>【Connection Management】，删除【SQLite - Chinook (Sample)】，避免遭受 SQL 注入攻击
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/en/cloudbeaver/cloudbeaver-wizard005-websoft9.png)

6. 再回到主页，默认的 SQLite 演示连接已经不存在

> More guide about CloudBeaver, please refer to [CloudBeaver Documentation](https://cloudbeaver.io/docs/).

## CloudBeaver Setup wizard

Coming soon...

## Q&A

#### Can't visit the start page of CloudBeaver?

Your TCP:80 of Security Group Rules is not allowed, so there is no response from Chrome or Firefox.

#### 是否可以禁止通过 80 端口访问 CloudBeaver ？

可以，本部署方案通过 Nginx 进行转发访问 CloudBeaver （实际上是 9090 端口），修改 Nginx 配置即可
