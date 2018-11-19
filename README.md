# docker-taiga
Docker container for Taiga https://taiga.io

本仓库适合宿主机已有nginx做反向代理和SSL的情况。
## 配置taiga-front-dist
1. 按照Taiga官方文档在宿主机的nginx中配置反向代理和SSL。
2. 克隆并按照Taiga官方文档配置taiga-front-dist。 
## 快速开始
1. 如果只想试用本镜像，或者希望运行在本地或者开发环境，只需要在终端下输入：
```docker-compose up ```
> 这将会引入`docker-compose.yml`和`docker-compose.override.yml`
此时按照taiga-front-dist的nginx配置，在浏览器输入对应网址，就可以访问登录界面了，用户名为admin，密码为123123。
2. 生产环境,在终端下输入
```docker-compose -f docker-compose.yml -f docker-compose.production.yml up```

了解更多关于 [docker compose中的覆盖和扩展](https://docs.docker.com/compose/extends/#example-use-case)