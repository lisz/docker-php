## docker

> docker-compose 脚本模版

#### 安装步骤

1. 复制`docker-compose.yml.example`为`docker-compose.yml`
2. 修改`docker-compose.yml`配置： 
   1. `volumes`: 设置文件夹镜像
3. 执行`docker-compose up -d`，下载并启动镜像


#### 注意事项

- `nginx.conf`有改动需要手动复制到容器里面
```
docker cp ./nginx/nginx.conf nginx:/etc/nginx/nginx.conf
```

- 重启容器

```
docker-compose restart
```

- `docker-compose.yml`文件有变动需要重新装载容器

```
docker-compose up -d
```


#### 文件结构

```bash
│  .gitignore
│  docker-compose.yml.example
│  README.md
│
├─mysql  # mysql目录
│  ├─conf.d # 配置项
│  │      mysqld.cnf
│  │
│  ├─data #  数据
│  │      .gitignore
│  │
│  └─logs # 日志
│          .gitignore
│
├─nginx # nginx目录
│  │  nginx.conf # 主配置项
│  │
│  ├─conf.d # 配置项
│  │      .gitignore
│  │      default.conf # 默认配置 localhost
│  │
│  └─ssl # 证书目录
│          .gitignore
│
└─php # PHP目录
    └─conf.d # 配置项
            php.ini
```

