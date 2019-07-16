# docker

docker-compose 

### 安装步骤

1. 复制`docker-compose.yml.example`为`docker-compose.yml`
2. 修改`docker-compose.yml`配置： 
   1. `volumes`: 设置文件夹镜像
3. 执行`docker-compose up -d`，下载并启动镜像



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

