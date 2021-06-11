# CloudBeaver Community

## Nginx 配置

```
  location / {
    proxy_pass       http://localhost:8978;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header Host $http_host;
  }
```

## 体验

* 安装 SQLite，便于测试
* 安装 Nginx，便于用户做更多访问控制

## 版本

CloudBeaver 版本查询方法未知。但可以通过 https://hub.docker.com/r/dbeaver/cloudbeaver/tags 查看
