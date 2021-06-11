# 初始化安装

在云服务器上部署 CloudBeaver 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:80** 端口是否开启
3. 若想用域名访问 CloudBeaver，请先到 **域名控制台** 完成一个域名解析

## CloudBeaver 安装向导

1. 使用本地电脑浏览器访问网址：*http://域名* 或 *http://服务器公网IP*, 进入初始化页面
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/zh/cloudbeaver/cloudbeaver-wizard001-websoft9.png)

2. 设置用户名和密码，然后点击【Next】进入下一步
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/zh/cloudbeaver/cloudbeaver-wizard002-websoft9.png)

3. 继续点击【Next】进入下一步，最后点击【FINISH】完成初始化
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/zh/cloudbeaver/cloudbeaver-wizard003-websoft9.png)

4. 默认已经存在一个 SQlite 的演示连接
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/zh/cloudbeaver/cloudbeaver-wizard004-websoft9.png)

5. 通过：【Administrator】>【Connection Management】，删除【SQLite - Chinook (Sample)】，避免遭受 SQL 注入攻击
   ![初始化 CloudBeaver](https://libs.websoft9.com/Websoft9/DocsPicture/zh/cloudbeaver/cloudbeaver-wizard005-websoft9.png)

6. 再回到主页，默认的 SQLite 演示连接已经不存在

> 需要了解更多 CloudBeaver 的使用，请参考[官方文档](https://cloudbeaver.io/docs/)

## CloudBeaver 入门向导

现在开始针对于如何使用 CloudBeaver 管理数据库，进行完整的说明：

## 常见问题

#### 浏览器打开IP地址，无法访问 CloudBeaver（白屏没有结果）？

您的服务器对应的安全组 80 端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容

#### 是否可以禁止通过 80 端口访问 CloudBeaver ？

可以，本部署方案通过 Nginx 进行转发访问 CloudBeaver （实际上是 9090 端口），修改 Nginx 配置即可
